# CASO 20 — Previsión de demanda y pedido óptimo para mayorista

## El problema que resuelve

Tu responsable de compras lleva 20 años pidiendo "lo de siempre" a cada proveedor. Su intuición era buena cuando el mercado era estable, pero hoy tienes:

- **89.000 € parados en sobrestock** (referencias con más de 180 días de cobertura).
- **8 referencias críticas en rotura semanal** — de ellas, 3 son producto clase A (las que más facturan).
- Pedidos que se hacen a ojo, sin cruzar el histórico de ventas con el plazo de proveedor ni con los pedidos que ya están en camino.

Resultado: capital inmovilizado, ventas perdidas por rotura, y decisiones de compra que dependen de una sola persona.

Este pack ejecuta un sistema de reaprovisionamiento profesional en 2 minutos: previsión de demanda a 4 semanas, punto de reorden, detección automática de sobrestock y rotura, y pedido óptimo agrupado por proveedor. Tu comprador pasa de adivinar a **revisar y validar**.

## Qué contiene el ZIP

| Archivo | Para qué sirve |
|---|---|
| `LEEME.md` | Este documento. Instrucciones y contexto. |
| `prompt.txt` | El prompt que pegarás en Claude Code. |
| `ventas_12m.csv` | Histórico de ventas semanales de los últimos 12 meses (60 referencias × 52 semanas). |
| `stock_actual.csv` | Stock actual por referencia, coste unitario, proveedor y plazo de entrega. |
| `pedidos_pendientes.csv` | Pedidos ya cursados que aún no han llegado. |

## Cómo usarlo — paso a paso

1. **Instala Claude Code** si aún no lo tienes: https://docs.claude.com/claude-code (necesitas cuenta Claude Pro o Max).
2. **Descomprime este ZIP** en una carpeta de tu equipo. Recomendado: `C:\Users\[tuusuario]\Downloads\Ejemplo Claude Code\Vídeo 20\`.
3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra a la ventana de Claude Code** el `LEEME.md` y el `prompt.txt`. Así la IA carga primero el contexto completo del caso.
5. **Abre el `prompt.txt`**, cambia las variables entre corchetes si quieres (nombre de tu empresa, mes, ruta) y **pega el contenido en Claude Code**.
6. Pulsa **Enter** y espera. En 2-3 minutos tendrás:
   - Un **dashboard HTML** que se abre en el navegador con alertas visuales.
   - Un **Excel** con todas las referencias analizadas, siguiendo el estilo corporativo de PlanillasExcel.es.
   - El **pedido óptimo por proveedor**, listo para que tu comprador lo revise.

## De dónde sacar los datos reales en tu ERP

Los 3 CSVs de este ejemplo son ficticios, pero se corresponden con datos que están en cualquier ERP. Aquí tienes dónde buscarlos:

**Ventas 12 meses (ventas_12m.csv):**
- **SAP Business One:** módulo Ventas → Informe de ventas por artículo → agrupado por semana.
- **A3 ERP / A3 Innuva:** Ventas → Estadísticas → Ventas por artículo y periodo.
- **Sage 50 / Sage 200:** Ventas → Consultas → Ventas por artículo → exportar a Excel.
- **Holded:** Ventas → Facturas → filtrar 12 meses → exportar CSV con detalle de líneas.
- **Odoo:** Ventas → Informes → Análisis de ventas → agrupar por producto y semana.

**Stock actual (stock_actual.csv):**
- Cualquier ERP: módulo de Almacén / Inventario → informe de stock por referencia con coste medio ponderado y proveedor principal.
- El **plazo de entrega** en días suele estar en la ficha maestra del proveedor o del artículo.

**Pedidos pendientes (pedidos_pendientes.csv):**
- Módulo de Compras → Pedidos de compra en estado "abierto" o "pendiente de recepción" → exportar con cantidad y fecha prevista.

Si tu ERP no exporta directamente en este formato, cualquier técnico o consultor te lo puede montar en 30 minutos con una consulta SQL. También puedes pedirle a Claude Code que te ayude a construir la consulta.

## Nota importante

Este caso está diseñado para **mayoristas y distribuidores** con catálogo de 500 a 5.000 referencias, plazo de entrega de proveedor conocido, y ventas con cierta recurrencia. Si tu negocio es de proyecto único, gran cuenta con contrato marco, o producto perecedero (frescos, farma), el modelo necesita ajustes: pídele a Claude Code que adapte el stock de seguridad y la ventana de previsión a tu caso.

También funciona bien en:
- Distribución de material industrial, ferretería, suministros.
- E-commerce con almacén propio y catálogo estable.
- Fabricantes que reponen componentes recurrentes.

---

Creado por Isaac Romà · https://isaacroma.com
