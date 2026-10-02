# Caso 06 — ¿Qué clientes son rentables y cuáles te cuestan dinero?

## El problema que resuelve

La mayoría de empresas de servicios (consultoras, asesorías, ingenierías, agencias) facturan por cliente pero **no cruzan las horas reales de su equipo con lo que cobran**. El resultado: clientes que parecen buenos porque facturan mucho, pero que en realidad consumen más recursos de los que generan.

Este caso analiza 8 clientes de una consultora ficticia ("Consulting Horizonte S.L.") y descubre que **el 2º cliente en facturación (4.200€/mes) cuesta 5.100€ en horas reales → pierde 900€/mes**.

Sin este análisis, estás vendiendo a ciegas.

---

## Qué contiene este ZIP

| Archivo | Descripción |
|---------|-------------|
| `LEEME.md` | Este archivo de instrucciones |
| `prompt.txt` | El prompt que pegarás en Claude Code |
| `horas_equipo.csv` | Horas mensuales por empleado y cliente (junio 2025) |
| `costes_empleado.csv` | Coste/hora y rol de cada empleado |
| `facturacion_clientes.csv` | Facturación mensual por cliente y tipo de contrato |

---

## Cómo usarlo paso a paso

### 1. Instala Claude Code (si no lo tienes)
```
npm install -g @anthropic-ai/claude-code
```
Necesitas Node.js 18+ y una cuenta en Anthropic con API key.

### 2. Copia los archivos CSV a una carpeta
Copia `horas_equipo.csv`, `costes_empleado.csv` y `facturacion_clientes.csv` a una carpeta de tu ordenador. Por ejemplo:
```
C:\Users\TU_USUARIO\Downloads\Ejemplo Claude Code\Vídeo 06\
```

### 3. Abre Claude Code
Abre tu terminal (CMD, PowerShell o Terminal en Mac) y escribe:
```
claude
```

### 4. Pega el prompt
Abre `prompt.txt`, copia todo el contenido y pégalo en Claude Code. **Antes de dar Enter**, cambia estas variables:

- `[EMPRESA]` → El nombre de tu empresa
- `[MES AÑO]` → El mes que quieres analizar (ej: "Junio 2025")
- `@ruta/` → La ruta donde están tus CSVs

### 5. Pulsa Enter y espera
Claude Code cruzará los tres archivos, calculará la rentabilidad de cada cliente y generará un dashboard HTML interactivo con semáforo y recomendaciones.

---

## ¿De dónde saco los datos en mi ERP?

### horas_equipo.csv
- **A3 Gestión / A3 Asesor**: Módulo de control horario → Informe de horas por empleado/proyecto
- **Sage 200**: Partes de trabajo → Exportar por cliente y empleado
- **Holded**: Gestión del tiempo → Informe por proyecto/cliente
- **SAP Business One**: Módulo de Proyectos → Informe de actividades
- **Odoo**: Hojas de tiempo → Exportar a CSV filtrando por cliente
- **Excel/manual**: Si llevas el control en hojas de cálculo, asegúrate de tener columnas: Empleado, Cliente, Horas, Mes

### costes_empleado.csv
- Nóminas o departamento de RRHH: coste empresa/hora de cada empleado
- Si no lo tienes exacto: (salario bruto anual + SS empresa) / (horas anuales trabajadas)
- Valor típico en España: entre 25€ y 60€/hora según perfil

### facturacion_clientes.csv
- **A3 / Sage / Holded / SAP**: Módulo de facturación → Informe por cliente y período
- **Odoo**: Contabilidad → Facturas emitidas por cliente
- Tu programa de facturación habitual → exporta por cliente y mes

---

## Nota importante

Este prompt está diseñado para **empresas de servicios profesionales** (consultoras, asesorías, despachos, agencias, ingenierías) donde el coste principal es el tiempo del equipo. Si tu empresa es industrial o comercial, el análisis de rentabilidad requiere incluir materiales, costes de producción y márgenes por producto — contacta con nosotros para adaptarlo.

---

Creado por **Isaac Romà** · [https://isaacroma.com](https://isaacroma.com)
