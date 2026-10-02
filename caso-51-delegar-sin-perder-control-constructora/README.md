# Caso 51 · Delegar sin perder el control — Panel por obra, flujo de aprobación por importe e informe semanal de una página

> El sistema que te deja solo ver las excepciones: dejas de pasar por 60-70 horas semanales y recuperas 15-20 h sin perder visibilidad sobre coste, caja y decisiones críticas.

## 🎯 Problema que resuelve

El gerente típico de una constructora de 1-50M€ no quiere microgestionar: lo hace porque si no revisa personalmente cada compra, cada presupuesto, cada incidencia en obra, el dinero se escapa. El resultado es una semana de 60-70 horas, un negocio que no crece porque el gerente es el cuello de botella de todas las decisiones y una empresa que se paraliza cuando él se va de vacaciones. El problema de fondo no es la falta de confianza en el equipo, sino la ausencia de un sistema que entregue solo las excepciones: hoy el jefe de obra manda la solicitud por WhatsApp, el director de producción la reenvía por email y el gerente aprueba una compra de 300 € con el mismo esfuerzo que una subcontrata de 25.000 €. Este pack usa Claude Code para montar en minutos la infraestructura mínima que permite delegar con datos y no con fe: un dashboard por obra con semáforos sobre avance, desviación de coste, caja, incidencias, retrasos y margen; un flujo de aprobación escalonado por importe (menos de 1K€ jefe de obra, 1-5K€ director de producción, más de 5K€ gerente); un dashboard HTML consolidado para ver todas las obras de un vistazo; y un informe semanal de una sola página con las excepciones que requieren decisión del gerente. Lo que entra en la mesa del gerente deja de ser el día a día y pasa a ser únicamente aquello que supera umbral o se desvía de plan.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía original del caso |
| `prompt.txt` | Prompt para pegar en Claude Code |
| `kpis_obra.csv` | 4 obras × 6 KPIs (avance, desviación, caja, incidencias, retrasos, margen) |
| `aprobaciones.csv` | 10 solicitudes pendientes con importe y nivel de escalado |

## 🚀 Cómo usarlo en 5 pasos

1. Instala Claude Code siguiendo la guía oficial en https://docs.anthropic.com/en/docs/claude-code y ejecutando `npm install -g @anthropic-ai/claude-code` (requiere Node.js).
2. Crea una carpeta con los 4 archivos del ZIP y abre la terminal allí.
3. Escribe `claude` y arrastra `LEEME.md` y `prompt.txt` a la conversación para dar contexto completo.
4. En `prompt.txt`, sustituye `[EMPRESA]`, `[MES AÑO]` y `[RUTA]` por tus datos reales.
5. Pega el prompt y pulsa Enter. Claude Code genera dashboard Excel por obra, dashboard HTML consolidado, HTML del flujo de aprobación e informe semanal HTML, y levanta un servidor local para abrirlos en el navegador.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | KPIs por obra | Aprobaciones / solicitudes |
|---|---|---|
| **Presto / CYPE / Menfis** | Certificación, control de coste y caja por obra | Flujo manual + Excel semanal |
| **A3 Innuva / Sage 50c Construcción** | Módulo Obras: avance, desviación, caja | Compras → Pedidos pendientes |
| **SAP Business One** | Project Management → Consulta de proyectos activos | Compras → Órdenes de compra para aprobar |
| **Holded** | Proyectos → Rentabilidad por proyecto | Compras → Facturas en borrador |
| **Odoo** | Proyectos → Panel de proyecto + Hojas de tiempo | Compras → Solicitudes de presupuesto |
| **Procore / Autodesk Construction Cloud** | Project financials → Export | Approvals → Export directo |

Columnas mínimas en `kpis_obra.csv`: id de obra, nombre, los 6 KPIs. En `aprobaciones.csv`: id de obra referenciada, solicitante, concepto, importe, tipo (compra/subcontrata/imprevisto). Si recoges las solicitudes por email o WhatsApp, dedica una tarde al volcado inicial y luego vas añadiendo semanalmente.

> ⚠️ **Nota de sector:** diseñado para constructoras y promotoras inmobiliarias españolas de 1-50M€, con los tramos típicos de aprobación (<1K€ jefe de obra / 1-5K€ dir. producción / >5K€ gerente). Para industria, servicios o distribución el flujo funciona igual, pero conviene ajustar nombres de KPI y tramos de importe a tu realidad. Si quieres cerrar el bucle de control por obra, encadénalo con [caso-45 (licitaciones obra pública)](../caso-45-licitaciones-obra-publica/), [caso-39 (posición financiera por obra)](../caso-39-posicion-financiera-por-obra/) y [caso-43 (dashboard ejecutivo semanal)](../caso-43-dashboard-ejecutivo-semanal/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años de C-Suite. Trabajo con PYMEs de 1-50M€ en industria, mayoristas y construcción.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 Reserva 30 min: https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>delegar sin perder control constructora, flujo de aprobación por importe pyme, dashboard obras semáforos kpis, panel gerente constructora 1-50M, informe semanal excepciones gerente, umbrales aprobación compra obra, recuperar horas gerente pyme construcción, control de obra automático claude code, sistema delegación constructora, consultor automatización gerencia pyme</sub>
