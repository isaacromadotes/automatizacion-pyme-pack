# Caso 46 · Equipo saturado: libera 20h/semana sin contratar — Detecta tareas automatizables en asesorías y despachos

> **Resultado:** El 60% del tiempo del equipo se va en tareas de bajo valor. Este caso identifica qué automatizar, cuántas horas liberas y cuánta capacidad extra ganas sin contratar. Web visual + Excel + plan de automatización en HTML.

## 🎯 Problema que resuelve

En asesorías, despachos profesionales, consultoras y agencias de marketing el socio se encuentra atrapado en una paradoja operativa: no puede captar más clientes porque el equipo está saturado, pero contratar es caro, formar al nuevo profesional lleva meses de rodaje y durante ese tiempo la calidad del servicio al resto de clientes cae porque los seniors dedican horas a formar en vez de a facturar. Mientras tanto se rechazan oportunidades de crecimiento o se atienden mal, y la rentabilidad por profesional se estanca o retrocede. Cuando se mide con rigor en qué se va realmente el tiempo del equipo —no la percepción del gerente, sino la realidad medida con tracker durante una semana— el patrón es muy consistente en todo el sector: alrededor del 60% de las horas se consumen en tareas de bajo valor directo que podrían automatizarse o estandarizarse (entrada manual de datos, conciliaciones bancarias repetitivas, recordatorios de cobro cliente a cliente, generación de facturas recurrentes mes a mes, archivo y etiquetado de documentos, respuestas estandarizadas por email, cuadres entre sistemas). El resto, el 40% restante, es el verdadero trabajo profesional que debería ser el núcleo del negocio y por el que el cliente paga. Este caso automatiza el análisis cruzando el listado de tareas que ejecuta el equipo, las horas semanales reales dedicadas a cada una y el coste/hora de cada profesional, clasifica cada tarea por potencial de automatización, cuantifica las horas liberables y el coste anual ahorrado, y entrega un plan de automatización priorizado con qué tecnología usar en cada caso (automatización simple vs IA vs rediseño de proceso) y capacidad extra que gana el equipo actual para absorber crecimiento.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `tareas_equipo.csv` | 19 tareas típicas de una asesoría |
| `costes_equipo.csv` | 6 personas con su coste/hora |
| `instrucciones_html.txt` | Guía de diseño para la web visual |
| `instrucciones_excel.txt` | Guía de diseño para el Excel |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_46_Saturacion_Equipo\`) con los 4 archivos en la raíz.
3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md`, `prompt.txt`, los 2 CSVs y los 2 TXT de instrucciones** al chat para dar contexto antes de ejecutar.
5. **Edita `prompt.txt`** cambiando `[EMPRESA]` y `[MES AÑO]`, pégalo y pulsa Enter. En 1-2 minutos tendrás web visual + Excel + plan de automatización en HTML.

## 🔌 Cómo exportar los datos desde tu ERP / control horario

| Software | Listado de tareas | Horas semanales | Coste/hora equipo |
|---|---|---|---|
| **A3ASESOR / A3 ERP (Wolters Kluwer)** | Gestión de tareas / Workflow | Control de tiempos | A3 Nom → Coste empresa ÷ horas útiles |
| **Sage Despachos Profesionales** | Tareas → Listado | Partes de trabajo | Sage Nom → Coste total ÷ horas |
| **Holded** | Proyectos → Tareas → Export | Timetracking proyectos | RRHH → Nómina ÷ horas convenio |
| **Odoo** | Proyecto → Tareas → Export CSV | Timesheets | RRHH → Coste empresa |
| **Toggl / Clockify** | — | Export por tarea y persona | Fórmula manual |
| **Factorial / Sesame** | — | Export horas trabajadas | Nómina → Coste empresa mensual |
| **SAP Business One** | Service → Actividades | Horas por contrato | HR Add-on → Coste empresa |
| **Sin ERP** | Hoja Excel compartida 1 semana | Toggl gratis o Excel | Fórmula: (Bruto anual + SS) ÷ 1.600 h |

**Fórmula coste/hora rápida:** Salario bruto mensual × 14 ÷ 1.600 h (aproximación). Más preciso: (Nómina bruta anual + SS empresa) ÷ 1.600 h efectivas.

> ⚠️ **Nota de sector:** Diseñado para **servicios profesionales** (asesorías, despachos de abogados, consultoras estratégicas, agencias de marketing, arquitectura, ingeniería). Para **PYMEs industriales o retail** la lógica funciona pero las categorías de tareas automatizables son otras (planificación de producción, picking, control de calidad, atención a pedido) → adapta `tareas_equipo.csv` al perfil operativo real. Para enlazar liberación de horas con rentabilidad por línea de servicio o cliente, combina con [caso-40 (rentabilidad por tipo servicio)](../caso-40-rentabilidad-por-tipo-servicio/) y [caso-28 (rentabilidad clientes asesoría)](../caso-28-rentabilidad-clientes-asesoria/): no basta con liberar horas, hay que redirigirlas a trabajo rentable.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** (y servicios profesionales) a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>liberar horas equipo asesoría, automatización tareas despacho profesional, capacidad extra sin contratar, Claude Code auditoría productividad, coste hora profesional servicios, tareas bajo valor asesoría contable fiscal, timetracking Toggl Clockify Factorial, rediseño procesos despacho, escalabilidad equipo asesoría, consultoría automatización servicios profesionales PYME España</sub>
