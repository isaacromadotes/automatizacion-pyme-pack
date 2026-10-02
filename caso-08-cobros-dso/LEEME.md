# Caso 08 — Sistema de Cobros y Reducción de DSO

## El problema

En muchas PYMEs mayoristas españolas, los cobros se gestionan de forma manual: alguien revisa las facturas vencidas en el ERP, envía recordatorios cuando se acuerda, y los pedidos siguen entrando aunque el cliente tenga deuda antigua. El resultado es un DSO (Days Sales Outstanding) disparado — habitualmente entre 75 y 90 días — que atrapa cientos de miles de euros en cuentas por cobrar.

En una empresa de 7M€ de facturación, pasar de un DSO de 78 a 54 días libera más de 450.000€ de liquidez inmediata.

## Qué contiene este ZIP

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Este archivo de instrucciones |
| `prompt.txt` | El prompt que pegarás en Claude Code |
| `facturas_emitidas.csv` | 127 facturas de ejemplo de "Suministros Levante S.L." |
| `maestro_clientes.csv` | 15 clientes con contacto, condiciones de pago y límite de crédito |

## Cómo usarlo paso a paso

### 1. Instala Claude Code
Si aún no lo tienes, sigue las instrucciones en https://docs.anthropic.com/en/docs/claude-code

### 2. Prepara tus archivos
Copia los dos CSVs (`facturas_emitidas.csv` y `maestro_clientes.csv`) a una carpeta accesible. Si quieres probar con tus datos reales, sustituye estos archivos manteniendo las mismas columnas.

### 3. Abre Claude Code y pega el prompt
Abre tu terminal, escribe `claude` y pega el contenido de `prompt.txt`. Antes de pulsar Enter:

- Sustituye `[EMPRESA]` por el nombre de tu empresa
- Sustituye `[MES AÑO]` por el periodo (ej: "Septiembre 2026")
- Ajusta la ruta `@ruta/` para que apunte a la carpeta donde tienes los CSVs

### 4. Pulsa Enter y espera
Claude Code analizará las facturas, calculará el DSO, clasificará la deuda por antigüedad, generará emails de reclamación escalonados, aplicará reglas de bloqueo y creará un dashboard web interactivo + entregables en Excel y PDF.

## De dónde sacar los datos en tu ERP

| ERP | Cómo exportar |
|---|---|
| **A3 (a3ERP / a3innuva)** | Contabilidad → Cuentas a cobrar → Exportar listado de facturas emitidas (CSV/Excel). Clientes desde Maestro de clientes |
| **Sage 200 / ContaPlus** | Informes → Cartera de efectos / Antigüedad de saldos → Exportar a Excel |
| **Holded** | Ventas → Facturas → Exportar CSV. Contactos → Exportar clientes |
| **SAP Business One** | Finanzas → Informe de antigüedad de deuda → Exportar. Socios de negocio → Exportar |
| **Odoo** | Contabilidad → Informes → Antigüedad de cuentas por cobrar → Exportar XLSX |

### Columnas necesarias

**facturas_emitidas.csv:**
`nro_factura`, `cliente`, `fecha_emision`, `fecha_vencimiento`, `importe_eur`, `estado`

**maestro_clientes.csv:**
`cliente`, `contacto_email`, `telefono`, `condiciones_pago_dias`, `limite_credito_eur`

## Nota importante

Este prompt está diseñado para el **sector mayorista / distribución**, donde el DSO alto y la morosidad recurrente son problemas frecuentes. Si tu empresa es de otro sector (fabricación, servicios, construcción), el prompt funciona igualmente — solo ajusta los nombres de las variables y las condiciones de pago habituales de tu sector.

---

Creado por Isaac Romà · https://isaacroma.com
