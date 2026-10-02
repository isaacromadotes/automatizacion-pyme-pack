# Caso 48 — Dependencia de clientes grandes

## El problema

El 55% de tu facturación viene de 3 clientes. Si uno se va, tu empresa tambalea.

La mayoría de PYMEs ni lo mide. Trabajan tranquilas creyendo que "va bien" hasta que un cliente grande se marcha y descubren que ese cliente aportaba el margen de todo el año.

Este pack mide la **concentración real de ingresos**, calcula qué pasa si pierdes al cliente más grande, y te da un plan concreto de diversificación: cuántos clientes nuevos necesitas y de qué tamaño medio.

## Qué contiene este ZIP

- `LEEME.md` → este archivo
- `prompt.txt` → el prompt que vas a pegar en Claude Code
- `datos/facturacion_cliente.csv` → ejemplo de facturación mensual por cliente (12 meses, 10 clientes)
- `datos/pipeline.csv` → ejemplo de pipeline comercial con prospectos y probabilidades

## Cómo usarlo (5 minutos)

1. **Instala Claude Code** si aún no lo tienes: https://claude.com/claude-code
2. **Descomprime este ZIP** en una carpeta de tu ordenador
3. **Sustituye los CSV de ejemplo** por los tuyos (mismo nombre, mismas columnas)
4. **Abre la terminal** en esa carpeta y escribe: `claude`
5. **Arrastra** `LEEME.md` y `prompt.txt` dentro de la conversación de Claude Code
6. **Pega el prompt.txt** y cambia estas variables:
   - `[EMPRESA]` → nombre de tu empresa
   - `[MES AÑO]` → mes y año actual (ej: Octubre 2026)
   - `@ruta/` → carpeta donde están tus CSV
7. **Pulsa Enter** y espera. Claude genera el dashboard web y el PDF.

## De dónde sacas los datos en tu ERP

Necesitas 2 exportaciones:

**Facturación por cliente** (`facturacion_cliente.csv`):
- **A3 ERP**: Ventas → Informes → Facturación por cliente → exportar a Excel → guardar como CSV
- **Sage 50/200**: Clientes → Informes → Ventas por cliente y mes → exportar CSV
- **Holded**: Ventas → Analítica → Por cliente → descargar CSV
- **SAP Business One**: Informes de ventas → Analítica por cliente → exportar
- **Odoo**: Facturación → Informes → Análisis de ventas → agrupar por cliente y mes → exportar CSV

Columnas que tiene que tener: `cliente`, `mes`, `importe`

**Pipeline comercial** (`pipeline.csv`):
- Sácalo de tu CRM (HubSpot, Pipedrive, Zoho, Holded CRM, Excel propio)
- Columnas: `prospecto`, `estado`, `importe_estimado`, `probabilidad`

## Para qué sector funciona

Este prompt está diseñado para **PYMEs de servicios, consultoría, agencias, despachos profesionales e industria B2B** donde la cartera de clientes activos es manejable (10-200 clientes) y hay riesgo real de concentración.

**No lo uses tal cual** si vendes B2C a miles de clientes pequeños (retail, ecommerce masivo, hostelería), ahí la concentración se mide distinto (por canal, categoría o producto).

---

Creado por Isaac Romà · https://isaacroma.com
