# Caso 34 · Detecta la fuga de clientes antes de que se vayan — Scoring de churn 0-100 para 400 clientes en minutos

> **Resultado:** Un cliente de 280 €/mes perdido son 3.360 € anuales de caja que desaparecen sin aviso. Este caso puntúa el riesgo de fuga de cada cliente cruzando interacciones, pagos, incidencias y antigüedad, y entrega dashboard con semáforos + PDF ejecutivo con las alertas más urgentes.

## 🎯 Problema que resuelve

En asesorías, despachos profesionales y cualquier negocio de servicios recurrentes B2B el churn silencioso es la mayor fuga de caja oculta: clientes que llevan años pagando una cuota mensual se dan de baja de repente y el gerente se entera cuando la administración detecta la devolución del recibo, momento en el que ya es imposible retener nada. El problema no es la falta de datos sino que nadie los cruza: el histórico de interacciones vive en el CRM o en las carpetas de Outlook, los pagos en el software contable, las quejas en una bandeja de emails sin estructurar y los contratos en una ficha estática que nadie revisa. Cuando se cruzan las cuatro señales (caída brusca de llamadas y emails, factura impagada sin reclamar, incidencia sin resolver durante semanas y antigüedad alta con cambios en el equipo del cliente) aparecen patrones muy claros: el cliente que antes contactaba 8 veces al mes ahora llama 1, lleva 60 días sin pagar sin que nadie le llame, tiene una queja de hace meses sin resolver y acumula 5 años de antigüedad —es decir, lleva meses hablando con la competencia aunque todavía nadie lo haya reconocido internamente—. Este caso automatiza ese cruce para toda la cartera (hasta 400 clientes en minutos), puntúa el riesgo de fuga de 0 a 100 por cliente, genera un dashboard HTML con semáforos verde/ámbar/rojo y entrega un PDF ejecutivo con las 3 alertas más urgentes y la acción de retención recomendada para cada una.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `interacciones_cliente.csv` | 9 meses de consultas, emails y llamadas por cliente |
| `pagos_cliente.csv` | Facturación y estado de pago |
| `incidencias.csv` | Quejas abiertas y cerradas |
| `contratos.csv` | Alta, cuota mensual y servicios contratados |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_34_Churn\`) con los 4 CSVs en la raíz.
3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md`, `prompt.txt` y los 4 CSVs** al chat para dar contexto completo antes de ejecutar.
5. **Edita `prompt.txt`** cambiando `[EMPRESA]`, `[MES AÑO]` y `@ruta/`, pégalo en Claude Code y pulsa Enter. Obtendrás validación de datos, dashboard HTML con semáforos y PDF ejecutivo con las 3 alertas más urgentes.

## 🔌 Cómo exportar los datos desde tu ERP / CRM

| Software | Interacciones | Pagos | Incidencias | Contratos |
|---|---|---|---|---|
| **A3ASESOR (Wolters Kluwer)** | CRM → Contactos por cliente | A3CON → Cartera de cobro | Módulo de incidencias (si activo) | Ficha cliente → Alta e iguala |
| **Sage Despachos / Sage 50** | Gestión Cliente → Historial | Cartera de cobro clientes | Módulo soporte | Ficha cliente → Cuota mensual |
| **Holded** | CRM → Actividades por contacto | Facturación → Listado por estado | Tickets / Tareas | Contactos → Campos personalizados |
| **Odoo** | CRM → Actividades por cliente | Contabilidad → Facturas abiertas | Helpdesk → Tickets | Suscripciones → Contratos activos |
| **HubSpot / Zoho CRM** | Export historial llamadas/emails | — (combinar con software contable) | Service Hub → Tickets | Deals / Negocios cerrados |
| **SAP Business One / Dynamics** | Actividades por socio de negocio | FBL5N / Antigüedad deudores | Service → Llamadas de servicio | Contratos de servicio |
| **Zendesk / Freshdesk / Jira SD** | — | — | Export de tickets por cliente | — |
| **Contasol / ContaPlus** | — | Vencimientos cliente (430) | — | Ficha cliente |

Si no tienes CRM, el **contador de emails por remitente en Outlook/Gmail** es un sustituto suficiente para la primera iteración.

> ⚠️ **Nota de sector:** Optimizado para **asesorías, despachos profesionales y servicios recurrentes B2B** (gestorías, agencias de marketing, SaaS con cuota mensual, mantenimientos, consultoras). Si tu modelo es B2C puro o venta transaccional sin recurrencia, los pesos del scoring deben recalibrarse —indícalo en el prompt y Claude Code lo ajustará—. Para enlazar la fuga de clientes con la rentabilidad real de cada cuenta, combina con [caso-28 (rentabilidad clientes asesoría)](../caso-28-rentabilidad-clientes-asesoria/): perder a un cliente deficitario puede ser buena noticia; perder a uno rentable es la señal a prevenir.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** (y despachos profesionales) a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>detección churn clientes asesoría, scoring riesgo fuga clientes B2B, retención clientes despacho profesional, Claude Code churn PYME servicios, señales abandono cliente recurrente, dashboard semáforo cartera clientes, automatización retención con IA, cross-selling CRM asesoría, análisis cartera gestoría consultoría, consultoría automatización servicios profesionales España</sub>
