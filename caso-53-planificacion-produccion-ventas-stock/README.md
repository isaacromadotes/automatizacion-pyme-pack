# Caso 53 · Planificación de producción conectada con ventas y stock — Plan semanal automático por línea con alertas de materia prima

> Cruza pedidos reales, stock de PT, capacidad de líneas y stock de MP para generar el plan semanal día a día y alertar antes de que la línea se pare.

## 🎯 Problema que resuelve

En la mayoría de PYMEs industriales y agroalimentarias la planificación de producción vive en un Excel que no habla con ventas ni con stock: el responsable abre los pedidos por un lado, mira el almacén por otro y lanza órdenes a ojo. El coste de esa desconexión aparece en todas direcciones: se fabrica de más lo que no se está vendiendo (sobrestock, caducidades, capital inmovilizado), se fabrica de menos lo que el cliente sí necesita (roturas, pedidos tarde, penalizaciones logísticas), se descubre que falta una materia prima cuando la línea ya está parada y las secuencias de producción no están optimizadas, de modo que cada cambio de formato cuesta tiempo y margen. El problema no es la falta de datos — los pedidos, el stock, la capacidad y los escandallos están en el ERP — sino la ausencia de un cruce semanal que convierta todo eso en un plan ejecutable. Este pack usa Claude Code para construir ese plan: lee pedidos abiertos de la semana, stock de producto terminado, capacidades y compatibilidades de las líneas y stock de materias primas con sus consumos unitarios, calcula qué fabricar, en qué línea, en qué secuencia y en qué día, minimiza cambios de formato, detecta antes qué MP se va a quedar corta y entrega un Excel semanal día a día por línea más un HTML local con las alertas accionables.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía original del caso |
| `prompt.txt` | Prompt para pegar en Claude Code |
| `pedidos_semana.csv` | 12 pedidos abiertos de ejemplo |
| `stock_pt.csv` | Stock de producto terminado |
| `capacidad_lineas.csv` | Capacidades y compatibilidades de 3 líneas |
| `stock_mp.csv` | Stock de materias primas y consumos |
| `diseño_excel.txt` | Diseño del Excel del plan semanal |
| `diseño_html.txt` | Diseño del HTML de alertas |

## 🚀 Cómo usarlo en 5 pasos

1. Instala Claude Code siguiendo la guía oficial en https://docs.anthropic.com/en/docs/claude-code y ejecutando `npm install -g @anthropic-ai/claude-code` (requiere Node.js).
2. Descomprime el ZIP en una carpeta (ej. `C:\Planificacion\`) y abre la terminal allí.
3. Escribe `claude` y arrastra `LEEME.md`, `prompt.txt`, los 4 CSV y los 2 TXT de diseño a la conversación.
4. En `prompt.txt`, sustituye `[EMPRESA]`, `[SEMANA AÑO]` (ej. "Semana 40 2026") y `@ruta/` por tus datos.
5. Pega el prompt y pulsa Enter. En 1-2 minutos tendrás el Excel con el plan día a día por línea y el HTML de alertas de materia prima listo para abrir en el navegador.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Pedidos abiertos | Stock PT | Capacidad líneas | Stock MP |
|---|---|---|---|---|
| **SAP Business One** | Ventas → Pedidos abiertos por fecha entrega | Inventario → Existencias almacén PT | Producción → Recursos / Centros | Inventario → Existencias almacén MP |
| **Sage 50/200** | Gestión comercial → Pedidos cliente "Pendiente" | Stocks → Existencias por almacén | Fabricación → Maestro de recursos | Stocks → Existencias MP |
| **A3 ERP** | Ventas → Pedidos pendientes de servir | Almacén → Stock valorado | Mantener manual (una vez) | Almacén → Stock MP |
| **Holded** | Ventas → Pedidos → Exportar CSV | Inventario → Existencias | Mantener manual | Inventario → MP |
| **Odoo** | Ventas → Pedidos "A entregar" | Inventario → Valoración | Fabricación → Centros de producción | Inventario → Valoración MP |
| **Navision / Business Central** | Pedidos de venta → Vista "Abiertos" | Almacenes → Existencias | Producción → Centros de trabajo | Almacenes → Existencias MP |

Columnas mínimas en `pedidos_semana.csv`: cliente, referencia, cantidad, fecha de entrega. En `stock_pt.csv`: referencia, descripción, stock actual, stock mínimo. En `capacidad_lineas.csv`: línea, productos compatibles, uds/turno, turnos/día, tiempo de cambio. En `stock_mp.csv`: materia prima, stock, consumo por 1.000 uds (sale del escandallo/BOM).

> ⚠️ **Nota de sector:** diseñado para PYMEs agroalimentarias e industriales con 2-5 líneas de producción y referencias que compiten por capacidad. En servicios o fabricación unitaria bajo pedido el enfoque es distinto. Para cerrar el bucle con la cadena de valor completa, encadénalo con [caso-47 (alerta variación coste materia prima)](../caso-47-alerta-variacion-coste-materia-prima/), [caso-50 (stock sin rotación)](../caso-50-stock-sin-rotacion/), [caso-37 (coste real PYME industrial)](../caso-37-coste-real-pyme-industrial/) y [caso-41 (auditoría IFS v8 agroalimentario)](../caso-41-auditoria-ifs-v8-agroalimentario/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años de C-Suite. Trabajo con PYMEs de 1-50M€ en industria, mayoristas y construcción.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 Reserva 30 min: https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>planificación producción semanal pyme, plan maestro producción agroalimentario, MRP ligero pyme industrial, alertas materia prima línea parada, secuenciación líneas producción conservera, cruzar pedidos stock capacidad automático, Excel plan producción claude code, consultor automatización producción pyme, evitar roturas y sobrestock industria, optimización cambios de formato línea</sub>
