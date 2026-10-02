# Caso 54 · Cobros se retrasan sin seguimiento sistemático — Baja tu DSO 15 días y libera caja sin vender un euro más

> Una consultora de 2M€ con DSO de 70 días tiene 390.000 € atrapados en cuentas a cobrar. Reducir el DSO 15 días libera 83.000 € en tesorería.

## 🎯 Problema que resuelve

La empresa factura bien pero cobra tarde porque nadie persigue las facturas vencidas de forma sistemática: el DSO sube de 45 a 70, a 90, a 120 días, la tesorería se tensa, hay que ampliar póliza de crédito, se pagan intereses y, mientras tanto, convive una lista de clientes que llevan meses sin pagar y a los que nadie ha reclamado en firme. El origen no suele ser la mala fe del cliente, sino la ausencia de un circuito: no hay aging segmentado por tramos (0-30, 31-60, 61-90, +90), no hay escalado de reclamación con tono creciente, no hay dashboard con el DSO real por cliente ni regla de bloqueo de servicio para morosos crónicos, y por tanto la persecución del cobro depende de que alguien del equipo tenga un rato libre y buena memoria. Este pack usa Claude Code para montar el sistema completo en minutos: lee facturas pendientes e histórico de pagos, calcula aging y DSO real por cliente, construye un panel HTML con semáforos para dirección y comercial, genera tres plantillas de email de reclamación escalonadas (cordial, firme y ultimátum), define una regla de bloqueo automático de servicio para clientes crónicamente morosos y entrega un PDF con la proyección de caja liberada si se cumple el plan. El objetivo no es cobrar más agresivo: es cobrar antes y de forma predecible.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía original del caso |
| `prompt.txt` | Prompt para pegar en Claude Code |
| `facturas_pendientes.csv` | 12 facturas pendientes de ejemplo |
| `historial_pagos.csv` | DSO histórico medio por cliente |
| `diseno.txt` | Guía de estilo del panel HTML |

## 🚀 Cómo usarlo en 5 pasos

1. Instala Claude Code siguiendo la guía oficial en https://docs.anthropic.com/en/docs/claude-code y ejecutando `npm install -g @anthropic-ai/claude-code` (requiere Node.js).
2. Descomprime el ZIP en una carpeta (ej. `~/CobrosClaude/`) y sustituye los CSV de ejemplo por los tuyos manteniendo nombres y columnas.
3. Abre la terminal en esa carpeta, escribe `claude` y arrastra `LEEME.md` y `prompt.txt` a la conversación.
4. En `prompt.txt`, sustituye `[EMPRESA]`, `[MES AÑO]` (ej. "Octubre 2026") y `@ruta/` por tus datos.
5. Pega el prompt y pulsa Enter. Claude Code genera el panel HTML, lo arranca, y entrega el Excel con los emails escalonados, la regla de bloqueo y el PDF de proyección de caja.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Facturas pendientes de cobro | DSO histórico por cliente |
|---|---|---|
| **SAP Business One** | Business Partners → Cuentas por cobrar → Aging report | Analítica → Días medios de cobro |
| **Sage 50/200** | Ventas → Cartera de efectos → Pendientes → CSV | Analítica financiera → DSO cliente |
| **A3 ERP** | Ventas → Facturas → Pendientes de cobro → Excel | Informes gerencia → Plazo medio cobro |
| **Holded** | Facturación → Facturas de venta → Filtro "Pendiente" | Analítica → Cobros |
| **Odoo** | Contabilidad → Clientes → Facturas no pagadas | Informes → Edad del saldo cliente |
| **Contasol / ContaPlus** | Procesos → Cartera → Vencimientos pendientes | Informes → Plazo medio de cobro |

Columnas mínimas en `facturas_pendientes.csv`: cliente, nº factura, importe, fecha emisión, fecha vencimiento, email de contacto. Para `historial_pagos.csv`, si tu ERP no da el DSO calculado, usa (días desde emisión hasta cobro) / número de facturas cobradas.

> ⚠️ **Nota de sector:** diseñado para PYMEs de servicios (consultoría, asesoría, agencias, SaaS B2B) con ciclo 30/60/90 días. En construcción amplía los umbrales a 60/90/120 (los pagos suelen ir a certificaciones). En industria y distribución mantén umbrales pero añade descuento por pronto pago en la lógica. En comercio minorista no aplica (cobro al contado). Para completar la mirada financiera, encadénalo con [caso-30 (forecast tesorería 90 días)](../caso-30-forecast-tesoreria-90-dias/), [caso-32 (forecast tesorería mayorista)](../caso-32-forecast-tesoreria-mayorista/) y [caso-35 (estacionalidad tesorería agroalimentario)](../caso-35-estacionalidad-tesoreria-agroalimentario/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años de C-Suite. Trabajo con PYMEs de 1-50M€ en industria, mayoristas y construcción.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 Reserva 30 min: https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>reducir DSO pyme servicios, aging facturas automático, emails reclamación escalonados cordial firme ultimátum, regla bloqueo servicio moroso crónico, liberar caja cuentas por cobrar, dashboard cobros semáforos pyme, consultor automatización tesorería claude code, seguimiento sistemático facturas vencidas, proyección caja reducción DSO, cobro predecible consultoría asesoría</sub>
