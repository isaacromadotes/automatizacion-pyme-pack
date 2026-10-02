# Caso 10 — Vencimientos fiscales controlados con Claude Code

## El problema que resuelve

Gestorías y asesorías con 200-500 clientes que gestionan vencimientos fiscales con agenda de papel, Excel manual o de memoria. Cada trimestre se escapan plazos, llegan sanciones y el gestor vive en modo bombero.

Este prompt cruza automáticamente tu cartera de clientes con el calendario fiscal, calcula TODOS los vencimientos del mes, genera emails de aviso (al gestor y al cliente) y lo presenta en un dashboard HTML interactivo con filtros, gráficos y semáforo de urgencias.

---

## Qué contiene este ZIP

| Archivo | Descripción |
|---|---|
| `prompt.txt` | El prompt que pegarás en Claude Code |
| `clientes_fiscal.csv` | Lista de 50 clientes ficticios con CIF, gestor, régimen IVA y tipo de sociedad |
| `calendario_fiscal.csv` | Calendario de obligaciones fiscales con modelos, plazos y a quién aplica cada uno |
| `LEEME.md` | Este archivo con instrucciones |

---

## Cómo usarlo paso a paso

### 1. Instala Claude Code (si no lo tienes)
```
npm install -g @anthropic-ai/claude-code
```
Necesitas Node.js 18+ y una cuenta de Anthropic con API key.

### 2. Copia los archivos CSV a una carpeta
Ejemplo: `C:\Users\TuUsuario\Descargas\fiscal\`

Coloca ahí:
- `clientes_fiscal.csv`
- `calendario_fiscal.csv`

### 3. Abre Claude Code
```
claude
```

### 4. Arrastra o pega el prompt
Abre `prompt.txt`, copia todo el contenido y pégalo en Claude Code.

**IMPORTANTE:** Antes de dar Enter, cambia estas variables:
- `[EMPRESA]` → el nombre de tu asesoría (ej: "Asesoría Martínez")
- `[MES AÑO]` → el mes que quieres controlar (ej: "Julio 2025")
- `@ruta/` → la ruta real donde tienes los CSVs (ej: `@C:\Users\TuUsuario\Descargas\fiscal\`)

### 5. Pulsa Enter y espera
Claude Code:
1. Validará los datos de ambos CSV
2. Cruzará clientes × obligaciones fiscales
3. Calculará todos los vencimientos del mes
4. Generará los emails de aviso
5. Creará un dashboard HTML profesional
6. Lo abrirá en tu navegador automáticamente

---

## De dónde sacar los datos reales en tu ERP

### clientes_fiscal.csv
| Campo | Dónde encontrarlo |
|---|---|
| empresa, cif | Ficha de cliente en cualquier ERP |
| gestor_asignado | Asignación interna de tu asesoría |
| email_cliente | Ficha de contacto del cliente |
| regimen_iva | A3 Asesor: Datos fiscales > Régimen IVA · Sage Despachos: Ficha empresa > Datos tributarios · Holded: Configuración > Impuestos |
| tipo_sociedad | Registro mercantil / escrituras del cliente |

### calendario_fiscal.csv
| Campo | Dónde encontrarlo |
|---|---|
| obligacion, modelo | Calendario del contribuyente de la AEAT (agenciatributaria.es) |
| fecha_limite | AEAT publica el calendario cada diciembre para el año siguiente |
| aplica_a | Según régimen fiscal de cada cliente |

**ERPs comunes:**
- **A3 Asesor / A3 ECO**: Exporta clientes desde Ficheros > Empresas. Régimen IVA en Datos Fiscales.
- **Sage Despachos**: Listado de empresas con filtro por tipo sociedad y régimen.
- **Holded**: Exporta desde Contactos > Clientes en CSV.
- **SAP Business One**: Informe de socios de negocio con campos fiscales.
- **Odoo**: Contactos > Exportar con campos fiscal_position y company_type.

---

## Nota importante

Este prompt está diseñado para **asesorías fiscales y gestorías** españolas. Los modelos tributarios (303, 111, 115, 130, 200, etc.) y los plazos corresponden al calendario de la **AEAT (Agencia Estatal de Administración Tributaria)**.

Si tu asesoría opera en un régimen foral (País Vasco, Navarra), deberás adaptar los modelos y plazos a la Hacienda Foral correspondiente.

El calendario fiscal incluido corresponde a **julio 2025** como ejemplo. Actualiza las fechas según el trimestre que necesites controlar.

---

Creado por Isaac Romà · https://isaacroma.com
