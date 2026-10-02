# Caso 36 · Leads que se pierden — Deja de tirar 9.000€/mes de facturación por el agujero multicanal

> **Resultado:** El 40% de los leads que entran a una PYME de servicios no se contactan en 24 h. Este caso unifica formulario web, email, teléfono y LinkedIn en un dashboard único con asignación automática al comercial, emails personalizados y alertas a las 24 h.

## 🎯 Problema que resuelve

En una PYME de servicios B2B los leads entran por cuatro canales distintos —formulario web, email corporativo, teléfono y LinkedIn— y cada canal se gestiona de forma independiente, con reglas, personas y herramientas distintas. El resultado es que el 40% de los leads no se contactan en las primeras 24 horas, momento clave en el que el prospecto todavía recuerda por qué dejó sus datos y tiene intención activa; pasadas 48 horas la probabilidad de conversión se hunde porque el lead ya ha hablado con dos o tres competidores. En una consultora que recibe 15 leads al mes significa 6 leads sin contactar, 3 oportunidades perdidas y aproximadamente 9.000 €/mes de facturación potencial tirada a la basura, cifra que escala linealmente conforme crece la empresa. El problema no es la falta de leads ni de comerciales: es la ausencia de un sistema único que capture, clasifique y asigne cada lead en minutos con reglas objetivas (zona geográfica, servicio de interés, carga actual del comercial, fit con el perfil) y que dispare automáticamente el primer email personalizado dentro de la primera hora. Este caso unifica los cuatro canales en un dashboard único, aplica reglas de scoring y asignación, genera emails de bienvenida y de seguimiento a 24/48 h a partir de plantillas con tono propio y emite alertas automáticas para cualquier lead sin tocar pasadas las 24 horas. El entregable incluye dashboard web interactivo y PDF resumen para dirección.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `csv/leads_mes.csv` | Leads de ejemplo recibidos por los 4 canales |
| `csv/comerciales.csv` | Equipo comercial con zonas y servicios que domina |
| `csv/plantillas_email.csv` | Plantillas de bienvenida y seguimiento 24h/48h |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_36_Leads\`) manteniendo la subcarpeta `csv/` tal cual.
3. **Abre la terminal** en la carpeta raíz y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md` y `prompt.txt`** al chat para dar contexto antes de ejecutar.
5. **Edita `prompt.txt`** cambiando `[EMPRESA]`, `[MES AÑO]` y `@ruta/`, pégalo y pulsa Enter. Obtendrás dashboard web + PDF resumen con leads asignados y emails generados.

## 🔌 Cómo exportar los datos desde tu CRM / ERP

| Software | Leads recibidos | Equipo comercial | Plantillas email |
|---|---|---|---|
| **HubSpot** | Contactos → Filtro fecha → Export CSV | Usuarios → Export | Marketing Email → Templates |
| **Pipedrive** | Leads → Filtro fecha → Export | Usuarios → Export | — (gestión externa) |
| **Zoho CRM** | Leads → Vista lista → Export | Usuarios y perfiles | Templates → Export |
| **Odoo CRM** | CRM → Leads/Oportunidades → Export | RRHH → Comercial → Export | Marketing automation templates |
| **Holded CRM** | CRM → Leads → Export | Equipo → Export | — (gestión externa) |
| **Salesforce** | Leads → List view → Export | Users → Export | Email templates |
| **A3 ERP / Sage** | — (combinar con CRM) | Nómina → Filtro depto Comercial | — |
| **WPForms / Contact Form 7** | Entradas → Export CSV | — | — |
| **LinkedIn Sales Navigator** | Listas guardadas → Export contactos | — | — |
| **Mailchimp / Brevo / ActiveCampaign** | — | — | Templates → Copiar HTML/texto |

Si no tienes CRM, filtra el buzón de Gmail/Outlook por asunto ("contacto", "información", "presupuesto") y vuélcalo manualmente al CSV: suficiente para la primera iteración.

> ⚠️ **Nota de sector:** Diseñado para **PYMEs de servicios B2B** (consultoras, asesorías, despachos profesionales, agencias). Para **e-commerce/retail** cambia `servicio_interes` por `producto_interes` y adapta las plantillas al tono comercial. Para **industrial/fabricación** añade `volumen_estimado` al CSV para que la asignación priorice leads grandes. Para **hostelería y restauración** este flujo no aplica (el problema es la reserva, no el lead). Para enlazar con la retención de los clientes que sí entran, combina con [caso-34 (detección churn clientes)](../caso-34-deteccion-churn-clientes/): captar bien es la mitad del trabajo, retener es la otra.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** (y servicios profesionales) a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>gestión leads multicanal PYME servicios, asignación automática comercial CRM, respuesta lead 24 horas B2B, Claude Code automatización comercial, unificar leads formulario web email LinkedIn, plantillas email bienvenida seguimiento, dashboard leads consultora asesoría, scoring leads servicios profesionales, automatización ventas HubSpot Pipedrive Zoho, consultoría automatización comercial PYME España</sub>
