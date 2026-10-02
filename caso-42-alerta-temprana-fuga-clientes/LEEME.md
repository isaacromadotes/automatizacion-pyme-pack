# Caso 42 — Clientes buenos se van sin que sepamos por qué

## El problema

Pierdes 2-3 clientes buenos cada trimestre. Cuando te das cuenta, ya es tarde: la decisión de irse se tomó meses antes.

Las señales estaban ahí:
- Caída progresiva en reuniones, emails y llamadas.
- Retrasos crecientes en pagos.
- Una queja sin resolver que nadie escaló.

Nadie las cruzó. Nadie las miró.

Este caso resuelve exactamente eso: Claude Code cruza tus 3 fuentes de datos (CRM, cobros e incidencias), calcula un scoring de riesgo de fuga 0-100 por cliente y te avisa 3 meses antes de la fuga.

Resultado: retención proactiva de clientes rentables.

---

## Qué contiene este ZIP

- **LEEME.md** — este archivo.
- **prompt.txt** — el prompt que pegarás en Claude Code.
- **interacciones.csv** — datos ficticios de reuniones, emails, llamadas y consultas por cliente/mes.
- **pagos.csv** — facturas emitidas, vencimientos y fechas reales de cobro.
- **incidencias.csv** — quejas, errores y consultas con estado (resuelta/pendiente).

Los 3 CSVs son de una consultora ficticia (Consulting Horizonte S.L.) con 30 clientes y 6 meses de datos. Importes y nombres son coherentes entre archivos.

---

## Cómo usarlo paso a paso

1. **Instala Claude Code** (si aún no lo tienes). Guía oficial: https://docs.claude.com/claude-code
2. **Descomprime este ZIP** en una carpeta de tu equipo. Ejemplo: `C:\casos\caso_42\`
3. **Abre tu terminal** (iTerm, PowerShell, Terminal) y entra en esa carpeta: `cd C:\casos\caso_42\`
4. **Arranca Claude Code**: escribe `claude` y pulsa Enter.
5. **Arrastra a la terminal** estos 3 archivos para que Claude los lea como contexto:
   - LEEME.md (contexto del caso)
   - prompt.txt (metodología)
   - Los 3 CSVs
6. **Abre prompt.txt**, cambia las variables entre corchetes (`[EMPRESA]`, `[MES AÑO]`, `[RUTA]`) por tus datos reales.
7. **Pega el prompt** en Claude Code y pulsa Enter.
8. En 2-3 minutos tendrás: dashboard HTML abierto en el navegador + Excel con scoring + PDF ejecutivo con los 3 clientes de más riesgo.

---

## De dónde sacar tus datos reales (según tu ERP/CRM)

| Fuente        | Dónde está en tu stack habitual                                                    |
|---------------|------------------------------------------------------------------------------------|
| Interacciones | **HubSpot / Pipedrive / Salesforce** → exporta actividades por contacto/empresa. **Holded** → módulo CRM → exportar actividad. |
| Pagos         | **A3 / Sage 50 / ContaPlus** → mayor de clientes con fechas de vencimiento y cobro. **Holded** → facturas emitidas con estado y fecha de pago. **SAP B1** → informe de antigüedad de saldos. **Odoo** → módulo Contabilidad → facturas de cliente. |
| Incidencias   | **Zendesk / Freshdesk / Intercom** → exporta tickets por cliente. **Email + Excel** → si no tienes helpdesk, un simple registro manual sirve. |

**Formato esperado:** CSV UTF-8, con las columnas que usan los archivos de ejemplo. Si tus columnas se llaman distinto, Claude Code las adapta solo.

---

## ⚠️ Nota importante — Sector al que aplica

Este prompt está diseñado para **empresas de servicios B2B con cartera recurrente**:
- Consultoras y asesorías (fiscal, laboral, legal, estratégica).
- Agencias (marketing, diseño, comunicación).
- Despachos profesionales.
- Software/SaaS con cuenta nombrada.
- Mantenimientos, servicios técnicos y suscripciones B2B.

**No aplica directamente** a retail físico, e-commerce masivo o ticketing B2C (ahí la fuga se mide con cohortes y churn, no con señales por cliente). Si tu caso es ese, dímelo en una reunión y adaptamos la metodología.

---

Creado por Isaac Romà · https://isaacroma.com
