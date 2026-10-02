# Caso 07 — Diagnóstico de Inventario: Sobrestock y Riesgo de Rotura

## El problema que resuelve

Tienes 400.000€ en stock y no sabes cuánto sobra ni qué te va a faltar la semana que viene. El responsable de compras pide "por intuición", el almacén se llena de referencias que no se mueven y producción se para porque falta una pieza crítica. Este prompt analiza tu inventario completo, clasifica ABC, detecta sobrestock con el capital inmovilizado en euros y te avisa de las roturas antes de que paren la fábrica.

## Qué contiene este ZIP

| Archivo | Qué es |
|---------|--------|
| `prompt.txt` | El prompt que pegarás en Claude Code |
| `LEEME.md` | Este archivo de instrucciones |
| `maestro_articulos.csv` | Maestro de 150 referencias con stock, costes y lead times |
| `consumos_12m.csv` | Consumos mensuales de los últimos 12 meses (1.800 registros) |
| `ordenes_produccion.csv` | Órdenes de producción pendientes (8 órdenes, 91 líneas) |

## Cómo usarlo paso a paso

1. **Instala Claude Code** si no lo tienes: https://docs.anthropic.com/en/docs/claude-code
2. **Copia los 3 archivos CSV** a una carpeta de tu ordenador (por ejemplo `~/Descargas/inventario/`)
3. **Abre Claude Code** en terminal
4. **Arrastra o copia** el archivo `prompt.txt` y los 3 CSV a la conversación de Claude Code
5. **Cambia las variables** del prompt:
   - `[EMPRESA]` → el nombre de tu empresa
   - `[MES AÑO]` → el mes de análisis (ej: "Septiembre 2026")
   - `@ruta/` → la ruta donde tienes tus CSV
6. **Pulsa Enter** y deja que Claude trabaje (~2-3 minutos)
7. Recibirás: un dashboard web interactivo + un Excel con 4 pestañas + un PDF ejecutivo

## De dónde sacar los datos en tu ERP

| Dato | A3 | Sage | Holded | SAP | Odoo |
|------|-----|------|--------|-----|------|
| Maestro artículos | Almacén → Artículos → Exportar | Inventario → Artículos | Inventario → Productos | MM01/MM60 | Inventario → Productos → Exportar |
| Consumos 12 meses | Almacén → Movimientos → Filtrar salidas | Movimientos de almacén → Salidas | Inventario → Movimientos | MB52 + MC.9 | Inventario → Informes → Movimientos |
| Órdenes producción | Producción → Órdenes activas | Fabricación → Órdenes | Fabricación → Órdenes | CO03 lista | Fabricación → Órdenes de producción |

## Nota importante

Este prompt está optimizado para **empresas industriales y de fabricación** (metalurgia, plásticos, alimentación, packaging...). Si tu empresa es de distribución o comercio, ajusta los umbrales de cobertura en el prompt: el sobrestock en distribución suele medirse en semanas, no en meses.

---

Creado por Isaac Romà · https://isaacroma.com
