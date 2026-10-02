# Caso 36 — Leads que se pierden

## El problema (dolor real de PYME)

El 40% de los leads que entran a una PYME de servicios **no se contactan en las primeras 24 horas**. La mitad se pierde para siempre.

Entran por formulario web, email, teléfono y LinkedIn. Cada canal es un agujero por donde se escapan oportunidades: nadie asigna el lead a un comercial, nadie envía el email de bienvenida, nadie hace seguimiento a las 48h.

Para una consultora de servicios con 15 leads/mes, esto se traduce en:
- 6 leads sin contactar
- 3 oportunidades perdidas
- **~9.000€/mes de facturación tirada a la basura**

Este pack monta en minutos un sistema que unifica los 4 canales en un dashboard único con asignación automática al comercial, generación de emails personalizados y alertas de leads sin contactar en 24h.

---

## Qué contiene este ZIP

| Archivo | Para qué sirve |
|---|---|
| `LEEME.md` | Este documento. Arrástralo a Claude Code primero. |
| `prompt.txt` | El prompt que pegarás en Claude Code. |
| `csv/leads_mes.csv` | Leads de ejemplo recibidos por los 4 canales. |
| `csv/comerciales.csv` | Equipo comercial con zonas y servicios que domina. |
| `csv/plantillas_email.csv` | Plantillas de bienvenida y seguimiento 24h/48h. |

---

## Cómo usarlo (paso a paso)

1. **Instala Claude Code** si no lo tienes: https://claude.com/claude-code
2. **Descomprime este ZIP** en una carpeta de tu ordenador (ej. `C:\Casos\Caso36\` o `~/Casos/Caso36/`).
3. **Abre tu terminal** (iTerm en Mac, PowerShell o CMD en Windows) y navega a esa carpeta.
4. **Escribe `claude`** y pulsa Enter.
5. **Arrastra a la ventana de Claude Code** este `LEEME.md` y el `prompt.txt` para que la IA entienda el contexto completo.
6. **Abre `prompt.txt`**, cambia las variables entre corchetes (`[EMPRESA]`, `[MES AÑO]`, `@ruta/`) por los tuyos.
7. **Pega el prompt completo** en Claude Code y pulsa Enter.
8. Claude Code analizará los leads, los asignará, generará los emails y abrirá un dashboard web en tu navegador. Al final te entregará también un PDF resumen.

---

## De dónde sacar los datos reales en tu ERP/CRM

Si quieres repetir este flujo con los datos reales de tu empresa en lugar de los de ejemplo, aquí tienes dónde exportar cada archivo:

### `leads_mes.csv` — Leads recibidos
- **HubSpot** → Contactos → Filtra por fecha de creación → Exportar CSV
- **Pipedrive** → Leads → Filtrar por fecha → Exportar
- **Zoho CRM** → Leads → Vista de lista → Exportar
- **Odoo** → CRM → Leads/Oportunidades → Acción → Exportar
- **Holded** → CRM → Leads → Exportar
- **Formulario web (WordPress + WPForms/Contact Form 7)** → Entradas → Exportar CSV
- **LinkedIn Sales Navigator** → Listas guardadas → Exportar contactos
- **Email corporativo (Gmail/Outlook)** → Si no tienes CRM, filtra por asunto "contacto" o similar y vuélcalo manualmente

### `comerciales.csv` — Equipo comercial
- **Tu CRM** → Usuarios/Vendedores → Exportar
- **A3 / Sage Nómina** → Listado de empleados → Filtrar por departamento "Comercial" → Exportar
- Si tienes pocos comerciales, créalo a mano en Excel (5 min).

### `plantillas_email.csv` — Plantillas de respuesta
- Las plantillas que incluyes aquí ya son tuyas, no vienen de ningún sistema. Edítalas con el tono de tu empresa.
- Si usas **Mailchimp / Brevo / ActiveCampaign**, puedes copiarlas desde ahí.

---

## ⚠️ Nota importante sobre el sector

Este prompt está diseñado para **PYMES de servicios B2B** (consultoras, asesorías, despachos profesionales, agencias). Si tu negocio es:

- **E-commerce / retail** → cambia el campo `servicio_interes` por `producto_interes` y adapta las plantillas.
- **Industrial / fabricación** → añade un campo `volumen_estimado` al CSV de leads para que la asignación priorice leads grandes.
- **Hostelería / restauración** → este flujo no aplica; para ti el problema es la reserva, no el lead.

Si tu sector no es servicios B2B, pide a Claude Code que adapte el prompt antes de ejecutarlo.

---

Creado por Isaac Romà · https://isaacroma.com
