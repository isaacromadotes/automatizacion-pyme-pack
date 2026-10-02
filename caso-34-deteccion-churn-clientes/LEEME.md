# CASO 34 — Detecta la fuga de clientes antes de que se vayan

## El problema

Si tienes una asesoría, un despacho o cualquier negocio de servicios recurrentes, el **churn silencioso** es tu mayor fuga de caja: un cliente de 280 €/mes que se da de baja son **3.360 € anuales** que desaparecen sin aviso. Y lo peor: siempre lo ves cuando ya es tarde.

Las señales están en tus datos. Nadie las cruza:

- El cliente que **antes llamaba 8 veces al mes** ahora llama 1.
- Una **factura impagada** de hace 60 días que nadie reclama.
- Una **queja sin resolver** de abril que se perdió en un email.
- 5 años de antigüedad = alta probabilidad de que ya esté hablando con la competencia.

Este pack te da un sistema para **puntuar el riesgo de fuga de cada cliente (0-100)** cruzando esas 4 señales. En minutos. Para 400 clientes.

## Qué contiene el ZIP

- `LEEME.md` — este archivo.
- `prompt.txt` — el prompt que vas a pegar en Claude Code.
- `interacciones_cliente.csv` — 9 meses de consultas, emails y llamadas por cliente.
- `pagos_cliente.csv` — facturación y estado de pago.
- `incidencias.csv` — quejas abiertas y cerradas.
- `contratos.csv` — alta, cuota mensual y servicios contratados.

Los 4 CSV son **datos ficticios realistas** de una asesoría española con 8 clientes de muestra. Están cruzados: los nombres coinciden entre archivos. Entre ellos hay 3 clientes en zona roja que Claude Code detectará.

## Cómo usarlo (5 minutos)

1. **Instala Claude Code** si aún no lo tienes: https://docs.claude.com/en/docs/claude-code
2. Crea una carpeta en tu equipo y **mete dentro los 6 archivos** de este ZIP.
3. Abre Claude Code en esa carpeta: `claude` en la terminal.
4. **Arrastra `LEEME.md` y `prompt.txt`** a la ventana de Claude Code (así entiende el contexto completo antes de ejecutar).
5. **Abre `prompt.txt`**, cambia las variables entre corchetes por las tuyas:
   - `[EMPRESA]` → el nombre de tu asesoría.
   - `[MES AÑO]` → el mes de corte del análisis (ej: `septiembre 2026`).
   - `@ruta/` → la ruta de la carpeta donde están tus CSV.
6. **Pega el prompt** en Claude Code y pulsa Enter.
7. Claude Code validará los datos, calculará el scoring, abrirá un dashboard HTML con semáforos y generará un PDF ejecutivo con las 3 alertas más urgentes.

## De dónde sacar tus propios datos

Si quieres probarlo con tu cartera real, exporta estos 4 archivos desde tu software:

| CSV | De dónde en tu ERP |
|---|---|
| `interacciones_cliente.csv` | **A3 ASESOR / Sage Despachos**: módulo CRM o Gestión de Cliente → informe de contactos. **Holded / Odoo**: CRM → actividades por contacto. **HubSpot / Zoho CRM**: exportar historial de llamadas y emails por cliente. **Si no tienes CRM**: Outlook/Gmail → contador de emails por remitente. |
| `pagos_cliente.csv` | **A3 CON / Contaplus / Sage 50**: libro mayor de clientes o informe de cartera de cobro. **Holded / FacturaDirecta / Quipu**: módulo de facturación → listado de facturas con estado. **SAP / Dynamics**: FBL5N o informe de cuentas a cobrar. |
| `incidencias.csv` | **Zendesk / Freshdesk / Jira Service Desk**: exportar tickets. **A3 ASESOR**: módulo de incidencias si lo tienes activo. **Si gestionas quejas por email**: carpeta "Incidencias" + fecha de entrada y estado. |
| `contratos.csv` | **A3 ASESOR / Sage Despachos**: ficha de cliente → fecha de alta, cuota e iguala. **Holded / Odoo**: contactos → campos personalizados. **ERP propio**: tabla de clientes con fecha de alta y plan contratado. |

## Importante

Este prompt está **optimizado para asesorías, despachos profesionales y negocios de servicios recurrentes B2B** (gestorías, agencias de marketing, empresas de software con cuota mensual, mantenimientos, consultoras). Si tu modelo es B2C puro o venta transaccional (sin recurrencia), los pesos del scoring deberán recalibrarse — avísaselo a Claude Code en el prompt y lo ajustará.

---

Creado por Isaac Romà · https://isaacroma.com
