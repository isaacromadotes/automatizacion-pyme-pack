# Caso 43 · Dashboard ejecutivo automático para la reunión de dirección — Deja de decidir por intuición cada lunes

> **Resultado:** Comité de dirección con dashboard HTML + PDF listo cada lunes a las 7:00 cruzando ventas, producción, contabilidad y operaciones de la semana cerrada. Decisiones basadas en datos, no en memoria.

## 🎯 Problema que resuelve

En la mayoría de PYMEs industriales el comité de dirección se reúne cada lunes para pilotar la semana, pero lo hace con información fragmentada y desactualizada: el responsable financiero improvisa cifras de memoria o con un Excel sin cerrar, el jefe de producción habla de sensaciones ("vamos justos de carga"), comercial tira de intuición sobre pedidos pendientes y nadie tiene un cuadro común con los mismos números. El resultado es una reunión de dos horas que no decanta decisiones concretas, los mismos temas vuelven la semana siguiente, los problemas serios explotan porque nadie los vio venir en los datos operativos y las iniciativas de mejora se arrancan sin baseline para medir después si funcionan. El coste real son horas del equipo directivo (las más caras de la empresa) y, sobre todo, reacciones tardías: un pedido grande se escapa porque el plazo de producción se detectó tarde, un cliente clave entra en impago sin que nadie lo mencionara, una línea con sobrecarga crónica no se desatasca porque no aparece en la conversación. Este caso automatiza la generación semanal del cuadro de mando ejecutivo cruzando ventas, producción, contabilidad y operaciones de la semana cerrada, calcula KPIs comparados con la semana anterior y con objetivo, resalta las desviaciones significativas con semáforo y entrega dashboard HTML navegable para proyectar en reunión y PDF descargable para quien no asista. El objetivo operativo es que cada lunes a las 7:00 los cuatro CSVs se vuelquen (manual los primeros meses, automatizado después con Power Automate o scripts del ERP) y el comité empiece la reunión con los datos ya mirados.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `ventas_semana.csv` | Ventas semanales (cliente, producto, importe, margen, estado) |
| `produccion_semana.csv` | Producción (línea, planificado vs producido, defectos, paros) |
| `contabilidad_semana.csv` | Cobros, pagos y movimientos financieros de la semana |
| `operaciones_semana.csv` | KPIs operativos (pedidos pendientes, plazos, incidencias, absentismo) |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_43_Dashboard_Ejecutivo\`) con los 4 CSVs en la raíz.
3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md`, `prompt.txt` y los 4 CSVs** al chat para dar contexto antes de ejecutar.
5. **Edita `prompt.txt`** cambiando `[EMPRESA]`, `[SEMANA]` (ej. "Semana 40, 29 sept – 5 oct") y `@ruta/`, pégalo y pulsa Enter. Claude Code genera el dashboard HTML, lo abre en el navegador y exporta el PDF.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP / Fuente | Ventas semanales | Producción semanal | Contabilidad semanal | Operaciones semanales |
|---|---|---|---|---|
| **SAP Business One / S/4** | Ventas → Facturación por período | Módulo Production / MES | Finanzas → Movimientos semana | Service / incidencias + HR absentismo |
| **A3 ERP / A3CON (Wolters Kluwer)** | Facturación → Export semana | Fabricación → Partes semanales | Libro diario cobros/pagos | Pedidos pendientes + RRHH |
| **Sage 50 / Sage 200** | Ventas → Facturación semana | Producción → Partes de fabricación | Tesorería → Movimientos | Pedidos + Incidencias |
| **Holded** | Facturación → Filtro semanal | Partes de producción | Tesorería semana | Proyectos / tareas |
| **Odoo** | Ventas → Filtro período | MRP → Órdenes de producción | Contabilidad → Movimientos | Inventario / Helpdesk / RRHH |
| **Navision / Business Central** | Ventas → Export | Producción → Partes | Diario cobros/pagos | Pedidos + Dimensiones RRHH |
| **MES propio / Excel jefe planta** | — | Volcado manual semanal | — | — |
| **Contasol / ContaPlus** | Facturación emitida | — | Libro diario | — |

> ⚠️ **Nota de sector:** Diseñado para **PYMEs industriales de 1-50 M€** (metalúrgicas, mecanizados, químico, plásticos, alimentación industrial). Para **servicios profesionales** sustituye el bloque "Producción" por horas facturables y utilización del equipo; para **comercio y distribución**, por rotación de stock y pedidos servidos; para **construcción**, por avance de obra y certificaciones. Indícalo en el prompt y Claude Code adapta los KPIs. Para profundizar en bloques concretos del dashboard, combina con [caso-30 (forecast tesorería 90 días)](../caso-30-forecast-tesoreria-90-dias/) o [caso-32 (forecast tesorería mayorista)](../caso-32-forecast-tesoreria-mayorista/) para el bloque financiero, [caso-31 (mantenimiento correctivo)](../caso-31-mantenimiento-correctivo-industrial/) para OEE y paros, y [caso-37 (coste real industrial)](../caso-37-coste-real-pyme-industrial/) para margen por SKU.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>dashboard ejecutivo semanal PYME industrial, cuadro mando comité dirección, KPIs semana ventas producción tesorería, Claude Code reporting semanal, decisiones basadas en datos PYME, reunión lunes dirección industrial, OEE producción semanal, automatización business intelligence PYME, dashboard HTML PDF ERP, consultoría automatización industria metalúrgica España</sub>
