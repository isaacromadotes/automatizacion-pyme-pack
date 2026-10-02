# CASO 53 — Planificación de producción conectada con ventas y stock

## El problema que resuelve

En muchas PYMEs industriales y agroalimentarias, la planificación de producción vive en un Excel que **no habla con ventas ni con stock**. El responsable de producción abre pedidos por un lado, mira el almacén por otro y lanza órdenes "a ojo". Resultado:

- Se produce de más lo que **no se está vendiendo** (sobrestock, caducidades, inmovilizado)
- Se produce de menos lo que **el cliente sí necesita** (roturas, pedidos tarde, penalizaciones)
- Se descubre que **falta materia prima** cuando la línea ya está parada
- Cada cambio de formato en la línea cuesta tiempo y dinero porque la secuencia no está optimizada

Este pack te permite generar el **plan semanal de producción** cruzando pedidos reales, stock de producto terminado, capacidad de líneas y stock de materias primas. Todo automático, con alertas incluidas.

---

## Qué contiene este ZIP

| Archivo | Para qué sirve |
|---|---|
| `LEEME.md` | Este documento. Léelo primero. |
| `prompt.txt` | El prompt que vas a pegar en Claude Code. |
| `pedidos_semana.csv` | Pedidos abiertos de la semana (12 pedidos de ejemplo). |
| `stock_pt.csv` | Stock de producto terminado por referencia. |
| `capacidad_lineas.csv` | Capacidad y compatibilidades de las 3 líneas de producción. |
| `stock_mp.csv` | Stock de materias primas y consumos unitarios. |
| `diseño_excel.txt` | Instrucciones de diseño para el Excel del plan semanal. |
| `diseño_html.txt` | Instrucciones de diseño para el HTML local de alertas. |

---

## Cómo usarlo paso a paso

1. **Instala Claude Code** si aún no lo tienes: https://docs.claude.com/claude-code
2. **Descomprime este ZIP** en una carpeta de tu ordenador (por ejemplo `C:\Planificacion\` o `~/Planificacion/`).
3. **Abre tu terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra** a la ventana de Claude Code: `LEEME.md`, `prompt.txt`, los 4 CSVs y los 2 TXT de diseño. Así la IA entiende el contexto completo antes de ejecutar.
5. **Abre `prompt.txt`**, cambia las variables entre corchetes:
   - `[EMPRESA]` → nombre de tu empresa
   - `[SEMANA AÑO]` → semana que vas a planificar (ej: `Semana 40 2026`)
   - `@ruta/` → ruta de la carpeta donde has puesto los archivos
6. **Pega el prompt** en Claude Code y pulsa Enter.
7. En 1-2 minutos tendrás:
   - **Excel** con el plan semanal día a día por línea
   - **HTML local** con las alertas de materias primas (ábrelo en el navegador)

---

## De dónde sacar los datos reales en tu ERP

Cuando quieras hacerlo con **datos reales de tu empresa**, estos son los informes que necesitas exportar:

### `pedidos_semana.csv` → Pedidos de venta abiertos
- **SAP Business One**: Módulo Ventas → Informe de pedidos abiertos por fecha de entrega
- **A3 ERP**: Ventas → Pedidos pendientes de servir
- **Sage 50/200**: Gestión comercial → Pedidos de cliente → Filtrar por estado "Pendiente"
- **Holded**: Ventas → Pedidos → Exportar a CSV
- **Odoo**: Ventas → Pedidos → Filtro "A entregar"
- **Navision/Business Central**: Pedidos de venta → Vista "Abiertos"

### `stock_pt.csv` → Stock de producto terminado
- Cualquier ERP: Informe de **existencias por almacén** del almacén de PT
- Exporta: referencia, descripción, stock actual, stock mínimo

### `capacidad_lineas.csv` → Capacidad productiva
- Si tienes MES/MRP: Maestro de líneas / recursos
- Si no, créalo manualmente (una sola vez): por cada línea, apunta qué productos puede hacer, unidades por turno, turnos/día y tiempo de cambio de formato

### `stock_mp.csv` → Stock de materias primas
- ERP: Informe de existencias del almacén de MP
- Añade a mano el consumo por 1.000 uds de producto terminado (sale del escandallo / BOM)

---

## ⚠️ Nota importante

Este prompt está diseñado para **PYMEs agroalimentarias e industriales con 2-5 líneas de producción** y referencias que compiten por capacidad. Si tu empresa es de servicios o fabricación a pedido unitario, pide ayuda para adaptarlo.

Los datos del ejemplo son **ficticios** (conservera inventada). Sirven para que veas el entregable antes de conectarlo a tu ERP.

---

Creado por Isaac Romà · https://isaacroma.com
