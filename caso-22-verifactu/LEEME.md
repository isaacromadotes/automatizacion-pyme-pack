# Caso 22 — Factura Certificada VERIFACTU con Claude Code

## El problema

A partir de enero de 2027, **VERIFACTU es obligatorio** para todos los sistemas de facturación en España (RD 1007/2023). El 79% de las PYMEs aún no están adaptadas. Si eres asesor o gestor, eso significa que cientos de tus clientes necesitan cumplir y tú necesitas una solución que ofrecer.

El problema real: adaptar el software de facturación cuesta miles de euros, lleva meses y muchas PYMEs pequeñas no tienen presupuesto ni tiempo. Claude Code genera una factura certificada completa — XML, hash encadenado, QR de verificación y envío a AEAT — en minutos.

## Qué contiene este ZIP

| Archivo | Descripción |
|---------|-------------|
| `prompt.txt` | El prompt para pegar en Claude Code |
| `factura_cliente.csv` | Datos de la factura de ejemplo (emisor, receptor, 3 líneas con IVA) |
| `hash_anterior.txt` | Hash SHA-256 de la factura anterior (para encadenamiento) |
| `certificado_firma.txt` | Datos del certificado digital simulado |
| `LEEME.md` | Este archivo |

## Cómo usarlo paso a paso

### 1. Instala Claude Code (si no lo tienes)
```
npm install -g @anthropic-ai/claude-code
```

### 2. Copia los archivos a una carpeta
Mueve `factura_cliente.csv`, `hash_anterior.txt` y `certificado_firma.txt` a una carpeta de trabajo. Por ejemplo:
```
C:\Users\TuUsuario\Downloads\Ejemplo Claude Code\
```

### 3. Abre Claude Code
```
claude
```

### 4. Pega el prompt
Abre `prompt.txt`, copia todo el contenido y pégalo en Claude Code.

**Antes de pegar, cambia estas variables:**
- `[EMPRESA]` → el nombre de tu empresa o la de tu cliente
- `[MES AÑO]` → el periodo (ej: "Enero 2027")
- `@ruta/` → la ruta real de tu carpeta (ej: `@C:\Users\TuUsuario\Downloads\Ejemplo Claude Code\`)

### 5. Pulsa Enter y espera
Claude Code:
- Validará los datos de la factura
- Generará el XML con todos los campos obligatorios del RD 1007/2023
- Calculará el hash SHA-256 encadenado
- Creará el QR de verificación AEAT
- Simulará el envío a la AEAT
- Generará un HTML profesional con la factura + código XML visible
- Generará un PDF de la factura con QR

## De dónde sacar los datos reales en tu ERP

| ERP | Dónde están los datos |
|-----|----------------------|
| **A3** | Gestión de Ventas → Facturas emitidas → Exportar detalle |
| **Sage** | Ventas → Facturas → Exportar a CSV/Excel |
| **Holded** | Ventas → Facturas → Exportar |
| **SAP Business One** | Gestión de ventas → Factura de deudores → Exportar |
| **Odoo** | Contabilidad → Facturas de cliente → Exportar todo |
| **Contaplus/Sage Despachos** | Gestión → Facturas emitidas → Listado → Exportar |
| **FacturaDirecta** | Facturas → Exportar datos |

Para el hash anterior: cada factura genera un `hash_actual.txt`. Usa el de la última factura emitida como `hash_anterior.txt` de la siguiente.

## Nota importante

Este prompt está diseñado para el **sector de servicios profesionales y asesorías**, pero funciona para cualquier empresa que emita facturas. Los campos XML siguen el esquema oficial de la AEAT (SuministroLRFacturasEmitidas).

La simulación de envío a AEAT es **demostrativa**. En producción, el envío real requiere certificado digital válido y conexión al servicio web de la AEAT.

---

Creado por Isaac Romà · https://isaacroma.com
