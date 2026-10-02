# Caso 42 · Clientes buenos se van sin que sepamos por qué — Sistema de alerta temprana con 3 meses de antelación

> **Resultado:** Pierdes 2-3 clientes buenos cada trimestre y la decisión se tomó meses antes. Este caso te avisa 3 meses antes de la fuga con dashboard HTML + Excel scoring + PDF ejecutivo con los 3 clientes de más riesgo y protocolo de retención por nivel de alerta.

## 🎯 Problema que resuelve

En consultoras, agencias, despachos profesionales y servicios B2B con cartera recurrente, la pérdida de un cliente bueno nunca es un evento repentino: es el final de una secuencia de 3-6 meses durante los cuales las señales estaban todas sobre la mesa pero nadie las cruzó. El patrón es siempre el mismo: caída progresiva en reuniones periódicas con el responsable del cliente, descenso en volumen de emails y llamadas entrantes, retrasos crecientes en pagos sin que administración los escale, una queja o incidencia sin resolver que lleva semanas pasando de inbox en inbox y, finalmente, una llamada educada del cliente anunciando que "ha decidido reorganizar proveedores". Cuando llega esa llamada ya es tarde: el competidor lleva meses trabajando el cliente, la decisión interna del comité ya está tomada y cualquier intento de retención se limita a una rebaja de última hora que destruye margen sin salvar la cuenta. El problema no es la falta de datos sino la ausencia de un sistema que vigile continuamente las tres señales clave y dispare un protocolo de retención cuando convergen. Este caso, a diferencia de un scoring puntual, se diseña como **sistema de alerta temprana recurrente**: cruza CRM, cobros e incidencias de los últimos 6 meses, puntúa el riesgo 0-100, clasifica cada cliente por nivel de alerta (verde / amarillo / naranja / rojo) y entrega para cada caso en riesgo el protocolo concreto de retención (quién llama, con qué guion, en qué plazo y con qué margen de negociación), ejecutable mensualmente para no volver a enterarte tarde.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `interacciones.csv` | Reuniones, emails, llamadas y consultas por cliente/mes |
| `pagos.csv` | Facturas emitidas, vencimientos y fechas reales de cobro |
| `incidencias.csv` | Quejas, errores y consultas con estado (resuelta/pendiente) |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_42_Alerta_Fuga\`) con los 3 CSVs en la raíz.
3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md`, `prompt.txt` y los 3 CSVs** al chat para dar contexto antes de ejecutar.
5. **Edita `prompt.txt`** cambiando `[EMPRESA]`, `[MES AÑO]` y `[RUTA]`, pégalo y pulsa Enter. En 2-3 minutos obtendrás dashboard HTML + Excel scoring + PDF ejecutivo con protocolo de retención.

## 🔌 Cómo exportar los datos desde tu CRM / ERP

| Software | Interacciones | Pagos | Incidencias |
|---|---|---|---|
| **HubSpot** | Actividades por empresa → Export | — (combinar con software contable) | Service Hub → Tickets |
| **Pipedrive** | Actividades por organización | — (combinar con software contable) | — (combinar con helpdesk) |
| **Salesforce** | Activities por Account | — (combinar con software contable) | Service Cloud → Casos |
| **Zoho CRM** | Actividades por cuenta | — (combinar con software contable) | Zoho Desk → Tickets |
| **Holded** | CRM → Actividad por contacto | Facturación → Estado y fecha pago | Tareas / Tickets internos |
| **Odoo** | CRM → Actividades por cliente | Contabilidad → Facturas de cliente | Helpdesk → Tickets |
| **A3 ERP / Sage 50 / ContaPlus** | — (combinar con CRM) | Mayor cliente con vencimientos y cobros | — (combinar con helpdesk) |
| **SAP Business One** | Actividades por socio negocio | Antigüedad de saldos | Service calls |
| **Zendesk / Freshdesk / Intercom** | — | — | Export tickets por cliente |
| **Email + Excel** | Contador emails por remitente | — | Registro manual de quejas |

Si tus columnas se llaman distinto a los CSVs de ejemplo, Claude Code adapta el mapeo automáticamente.

> ⚠️ **Nota de sector:** Diseñado para **servicios B2B con cartera recurrente**: consultoras, agencias de marketing/diseño/comunicación, despachos profesionales, SaaS con cuenta nombrada, mantenimientos y suscripciones B2B. **No aplica** a retail físico, e-commerce masivo o ticketing B2C (ahí la fuga se mide con cohortes y churn agregado, no con señales por cliente). Si lo que buscas es un **scoring puntual único** sin pensar en recurrencia operativa, usa [caso-34 (detección churn clientes)](../caso-34-deteccion-churn-clientes/), que es la variante estática. Este caso-42 está pensado para integrarse en el **ciclo mensual de dirección comercial** como check recurrente. Para enlazar la retención con el margen real de cada cliente retenido, combina con [caso-28 (rentabilidad clientes asesoría)](../caso-28-rentabilidad-clientes-asesoria/) o [caso-40 (rentabilidad por tipo servicio)](../caso-40-rentabilidad-por-tipo-servicio/): retener a un cliente deficitario no siempre vale la pena.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** (y servicios profesionales) a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>alerta temprana fuga clientes B2B, sistema retención proactiva consultora, protocolo retención cuenta nombrada, Claude Code alerta churn mensual, señales abandono cliente servicios, dashboard semáforo cartera consultora, retención agencias despacho SaaS, cross-sell retención cliente rentable, ciclo mensual dirección comercial, consultoría automatización retención PYME servicios España</sub>
