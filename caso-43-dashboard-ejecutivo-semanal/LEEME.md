# Caso 43 — Dashboard ejecutivo automático para la reunión de dirección

## El problema

Cada lunes el comité de dirección se sienta a decidir con datos del mes pasado. El responsable financiero improvisa cifras, producción habla de memoria, ventas tira de intuición. Las decisiones se toman por sensación, no por información.

Resultado: horas de reunión que no decanta nada, reuniones que se repiten la semana siguiente, y problemas que explotan porque nadie los vio venir en los números.

## Qué contiene este ZIP

- `LEEME.md` — Este archivo.
- `prompt.txt` — El prompt que pegas en Claude Code.
- `ventas_semana.csv` — Datos de ventas semanales (cliente, producto, importe, margen, estado).
- `produccion_semana.csv` — Datos de producción (línea, planificado vs producido, defectos, paros).
- `contabilidad_semana.csv` — Cobros, pagos y movimientos financieros de la semana.
- `operaciones_semana.csv` — KPIs operativos (pedidos pendientes, plazos, incidencias, absentismo).

## Cómo usarlo paso a paso

1. **Instala Claude Code** desde https://claude.com/claude-code si aún no lo tienes.
2. **Crea una carpeta** en tu equipo, por ejemplo `C:\Dashboards\Semana42\`.
3. **Copia los 4 CSVs** del ZIP a esa carpeta.
4. **Abre tu terminal** y escribe `claude` para iniciar Claude Code.
5. **Arrastra el `LEEME.md` y el `prompt.txt`** a la ventana de Claude Code para que entienda el contexto completo.
6. **Pega el contenido del `prompt.txt`** y cambia las variables entre corchetes:
   - `[EMPRESA]` → nombre de tu empresa
   - `[SEMANA]` → semana que analizas (ej. "Semana 40, 29 sept – 5 oct")
   - `@ruta/` → la ruta donde pusiste los CSVs
7. **Pulsa Enter** y espera. Claude Code genera el dashboard HTML, lo abre en el navegador y después exporta el PDF.

## De dónde sacar los datos reales en tu ERP

- **Ventas**: módulo de facturación de A3, Sage 50, Holded, SAP B1 u Odoo. Exporta la semana cerrada en CSV.
- **Producción**: tu MES o el módulo de producción de SAP/Odoo. Si no tienes MES, un Excel semanal del jefe de planta sirve.
- **Contabilidad**: libro diario de cobros y pagos del ERP contable (A3CON, Sage, ContaPlus).
- **Operaciones**: lo que lleve el responsable de operaciones — pedidos pendientes, incidencias de calidad, absentismo de RRHH.

El objetivo es que cada lunes a las 7:00 estos 4 archivos se vuelquen automáticamente (power automate, script o manual los primeros meses) y Claude Code haga el resto.

## Nota importante

Este prompt está diseñado para **PYMEs industriales de 1 a 50M€** (metalúrgicas, mecanizados, químico, alimentación industrial). Si tu empresa es de servicios, comercio o construcción, cambia los KPIs del bloque "Producción" por los que correspondan a tu operación (horas facturables, tickets, obras activas, etc.) y pídeselo a Claude Code en el mismo prompt.

---

Creado por Isaac Romà · https://isaacroma.com
