# Caso 40 · Rentabilidad real por tipo de servicio — Descubre qué línea de servicio en tu despacho pierde dinero

> **Resultado:** Ranking Excel + gráfico + HTML con propuestas de ajuste cruzando horas reales × coste/hora × honorarios. Normalmente aparece que laboral o fiscal menor consumen más horas que lo que facturan, mientras contable premium sostiene al despacho entero.

## 🎯 Problema que resuelve

En asesorías y despachos profesionales (contable, fiscal, laboral, legal, auditoría) se cobra una cuota mensual por cliente y servicio, pero prácticamente ninguna firma mide cuántas horas reales consume cada línea de servicio. El resultado es un portfolio opaco donde se asume que el precio histórico cubre el coste, cuando en realidad el laboral acumula una carga constante de incidencias (nóminas con retroactivos, altas y bajas, reclamaciones TGSS, modificaciones de contrato, bajas médicas con cálculo complejo, cálculo de finiquitos no estándar) que convierten una cuota aparentemente razonable de 180 €/mes en una línea con margen negativo real; el fiscal se tensiona en campaña de IVA y en los cierres trimestrales de IRPF retenciones; el contable premium, en cambio, suele sostener el margen del despacho sin que nadie lo visibilice. El problema no es la rentabilidad agregada del despacho —muchos cierran bien el año— sino que detrás de ese agregado hay líneas que subvencionan a otras y clientes concretos que destruyen margen sistemáticamente dentro de líneas globalmente rentables. Este caso cruza las horas reales imputadas por gestor, cliente y servicio con el coste real por hora de cada profesional (salario bruto + SS empresa dividido entre horas productivas anuales) y los honorarios efectivamente facturados, devolviendo un ranking de rentabilidad por línea de servicio y por cliente, con propuestas concretas de ajuste: subida de tarifa, limitación de scope del servicio o reestructuración de la cuota.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `horas_servicio.csv` | Horas reales trabajadas por gestor, cliente, servicio y mes |
| `honorarios_servicio.csv` | Cuota mensual facturada por cliente y servicio |
| `costes_gestor.csv` | Coste/hora por gestor (bruto + SS / horas productivas) |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_40_Rentabilidad_Servicio\`) con los 3 CSVs en la raíz.
3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md`, `prompt.txt` y los 3 CSVs** al chat para dar contexto antes de ejecutar.
5. **Edita `prompt.txt`** cambiando `[EMPRESA]`, `[MES AÑO]` (ej. "enero-junio 2026") y `@ruta/`, pégalo y pulsa Enter. Obtendrás Excel con ranking + gráfico y HTML con propuestas de ajuste.

## 🔌 Cómo exportar los datos desde tu ERP

| Software | Horas por servicio | Honorarios por servicio | Coste/hora gestor |
|---|---|---|---|
| **A3ASESOR / A3 ERP (Wolters Kluwer)** | Control de tiempos → Export | Facturación servicios recurrentes | A3 Nom → Coste empresa / horas útiles |
| **Sage Despachos Connected** | Partes de trabajo | Contratos de servicios | Sage Nom → Coste total / horas productivas |
| **Holded** | Proyectos → Timetracking | Facturación recurrente | RRHH → Nómina / horas convenio |
| **Odoo** | Timesheets → Analítica | Subscriptions / Suscripciones | RRHH → Coste empresa |
| **SAP Business One** | Service → Horas por contrato | Contratos de servicio recurrente | HR Add-on → Coste empresa |
| **Contasol / ContaPlus** | — (combinar con Clockify/Toggl) | Facturación → Clientes recurrentes | Nóminas → Coste empresa mensual |
| **Clockify / Toggl + Excel** | Export tracker → Cruce manual con clientes | Listado facturación emitida | Fórmula: (Bruto anual + SS) ÷ 1.600 h |

**Fórmula coste/hora gestor:** (Salario bruto anual + SS empresa) ÷ (Horas productivas anuales ≈ 1.600 h).

> ⚠️ **Nota de sector:** Diseñado para **asesorías y despachos profesionales** (contable, fiscal, laboral, legal, auditoría, consultoría). Los servicios tipo (contabilidad, fiscal, laboral, asesoramiento recurrente) son los habituales del sector. Funciona igual para **arquitectura, ingeniería, agencias de marketing y despachos de abogados**: solo cambia los nombres de los servicios en los CSVs y Claude Code se adapta. Para enlazar con el análisis cliente a cliente dentro de cada línea, combina con [caso-28 (rentabilidad clientes asesoría)](../caso-28-rentabilidad-clientes-asesoria/); para detectar fuga de los clientes rentables, con [caso-34 (detección churn)](../caso-34-deteccion-churn-clientes/).

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** (y despachos profesionales) a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>rentabilidad por línea servicio asesoría, margen contable fiscal laboral despacho, coste hora gestor PYME servicios, Claude Code análisis despacho profesional, imputación horaria A3ASESOR Sage, pricing servicios recurrentes asesoría, subida honorarios laboral fiscal, rentabilidad gestoría consultoría, Timetracking Clockify Toggl despacho, consultoría automatización servicios profesionales España</sub>
