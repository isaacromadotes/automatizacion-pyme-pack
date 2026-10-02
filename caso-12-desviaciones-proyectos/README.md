# Caso 12 · Alerta temprana de desviaciones en proyectos — Protege tu margen antes de quemarlo

> **Resultado clave:** Cruza horas imputadas vs presupuesto y avance real por proyecto, y lanza alerta roja cuando la desviación supera el 10-15%. Detecta los proyectos que se te están yendo cuando aún puedes renegociar con el cliente o reasignar equipo.

## 🎯 Problema que resuelve

Diriges una consultora, asesoría, ingeniería, estudio de arquitectura o despacho profesional. Tus equipos imputan horas cada semana en el ERP, pero el control real del margen por proyecto vive en la cabeza del jefe de proyecto, no en un sistema. El resultado es siempre el mismo: a final de trimestre descubres que tres proyectos han consumido el 130% del presupuesto de horas y solo llevan el 60% de avance, el margen se ha evaporado y nadie te avisó a tiempo. Cuando lo detectas, ya es tarde para renegociar con el cliente, reasignar personal al proyecto o parar un alcance que se ha disparado. El problema de fondo no es la gente ni la herramienta: es que falta un sistema automático que cruce horas reales, presupuesto y avance semana a semana, y lance alertas antes de que el proyecto esté perdido. Este caso automatiza ese control: cálculo de consumo real por proyecto, cruce con presupuesto de horas y avance estimado, semáforo visual (verde <5% desviación, ámbar 5-10%, rojo >10%), ranking de proyectos en riesgo, informe de alertas en formato 9:16 para enviar al comité semanal y dashboard interactivo para dirección. Pensado para empresas de servicios profesionales de 1-50M€ donde el margen depende de cumplir las horas presupuestadas por proyecto.

## 📦 Archivos del pack

| Archivo | Descripción |
|---------|-------------|
| `LEEME.md` | Instrucciones de uso del caso |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `proyectos.csv` | 8 proyectos de ejemplo (Consulting Horizonte S.L.) |
| `horas_imputadas.csv` | 160 imputaciones por persona, proyecto y fecha |
| `instrucciones_para_crear_tabla_excel.txt` | Guía de estilo corporativo para el Excel |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** si aún no lo tienes: `npm install -g @anthropic-ai/claude-code` (requiere Node.js 18+ y cuenta Anthropic con API key). Guía oficial: [docs.anthropic.com/en/docs/claude-code](https://docs.anthropic.com/en/docs/claude-code)
2. **Descomprime el pack** en una carpeta de tu ordenador (ej: `C:\Users\TU_USUARIO\Downloads\Desviaciones\`).
3. **Abre tu terminal** (CMD, PowerShell o Terminal en Mac) y lanza `claude` desde la carpeta donde están los archivos.
4. **Pega el `prompt.txt`** y antes de pulsar Enter sustituye las variables: `[EMPRESA]` por el nombre de tu empresa, `[MES AÑO]` por el período a analizar (ej. "Septiembre 2026") y `@ruta/` por la ruta real de tus CSVs.
5. **Pulsa Enter y espera** (~2-3 min). Claude Code entrega dashboard web, Excel con formato corporativo e informe HTML de alertas en vertical 9:16 listo para enviar al comité.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Proyectos (presupuesto + avance) | Horas imputadas |
|-----|-----------------------------------|-----------------|
| **A3 (A3 ERP / A3 Innuva)** | Proyectos → Informes → Cartera de proyectos → Exportar CSV | Proyectos → Partes de horas → Exportar |
| **Sage 200 / Sage Despachos** | Análisis rentabilidad proyectos → Exportar Excel | Timesheet → Exportar partes |
| **Holded** | Proyectos → Vista tabla → Exportar | Team → Timesheet → Exportar |
| **SAP Business One** | Gestión de Proyectos → Consulta → Exportar | Transacción CATS → Exportar |
| **Odoo** | Proyecto → Vista lista → Exportar | Hojas de tiempo → Exportar todo |
| **Notion / ClickUp** | Database → menú ··· → Export CSV | Timesheet view → Export CSV |

⚠️ **Nota de sector:** Este caso está diseñado para **empresas de servicios profesionales** (consultoría, asesoría, ingeniería, arquitectura, despachos legales, agencias de marketing). Si tu negocio es **industrial o retail**, la lógica horas-vs-avance no aplica directamente — adapta el prompt a unidades producidas vs planificadas (industria) o ventas vs objetivo (retail). En **construcción**, usa el **Caso 09 · Partes de obra** que ya trae presupuesto MOD semanal. Los umbrales de alerta por defecto (10% / 15%) son estándar del sector pero puedes ajustarlos en el bloque "CONTEXTO DE LA EMPRESA" del prompt según tu tolerancia al riesgo.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con 20 años en C-Suite. Ayudo a PYMEs españolas de **1-50M€** (industria, mayoristas y construcción) a automatizar procesos ejecutivos y traducir operaciones a impacto financiero real (EBITDA, caja, margen).

- **Diagnóstico inicial:** 750€
- **Automatización a medida:** desde 4.500€
- **Acompañamiento mensual:** 300€/mes

👉 **Reserva 30 min gratis:** [calendly.com/asesor-online-ia/30min](https://calendly.com/asesor-online-ia/30min)

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>desviación proyectos consultoría, control margen por proyecto, alerta temprana sobrecoste, horas imputadas vs presupuesto, dashboard rentabilidad proyectos, automatización servicios profesionales PYME, Claude Code consultora, consultor IA España, semáforo proyectos en riesgo, control de producción despacho</sub>
