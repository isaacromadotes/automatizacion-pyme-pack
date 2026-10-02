# Caso 48 · Dependencia de clientes grandes — Mide tu concentración real y cuántos clientes nuevos necesitas para dejar de depender

> Si el 55% de tu facturación viene de 3 clientes, calcula el impacto exacto de perder al mayor y recibe un plan de diversificación cuantificado.

## 🎯 Problema que resuelve

La mayoría de PYMEs trabaja tranquila creyendo que "va bien" hasta que un cliente grande se marcha y descubren, demasiado tarde, que ese cliente aportaba el margen de todo el año. El origen del problema casi nunca es la pérdida en sí, sino el hecho de no haberla medido antes: nadie en la empresa sabe qué porcentaje real pesa cada cliente, ni cuál es la caída de EBITDA si el top 1 se va, ni cuántos clientes nuevos del tamaño medio actual harían falta para compensar. Sin ese dato, el equipo comercial sigue persiguiendo las mismas cuentas grandes porque son las que mejor convierten, y la concentración se agrava en lugar de reducirse. Este pack usa Claude Code para medir la concentración real de ingresos sobre los últimos 12 meses, calcular el índice de dependencia (HHI y % top 1, top 3, top 5), simular qué pasa con la facturación y el margen si pierdes al cliente más grande, cruzar el gap resultante con tu pipeline actual y entregar un plan concreto de diversificación: cuántos prospectos necesitas cerrar, de qué ticket medio y en qué plazo para bajar la dependencia a un umbral sano. Salida: dashboard web + PDF ejecutivo para dirección y comité comercial.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía original del caso |
| `prompt.txt` | Prompt para pegar en Claude Code |
| `datos/facturacion_cliente.csv` | Facturación mensual por cliente (12 meses × 10 clientes) |
| `datos/pipeline.csv` | Pipeline comercial con prospectos y probabilidades |

## 🚀 Cómo usarlo en 5 pasos

1. Instala Claude Code siguiendo la guía oficial en https://docs.anthropic.com/en/docs/claude-code y ejecutando `npm install -g @anthropic-ai/claude-code` (requiere Node.js).
2. Descomprime el ZIP en una carpeta y sustituye los CSV de ejemplo por los tuyos, respetando nombres y columnas.
3. Abre la terminal en esa carpeta, escribe `claude` y arrastra `LEEME.md` y `prompt.txt` a la conversación.
4. Abre `prompt.txt` y sustituye `[EMPRESA]`, `[MES AÑO]` y `@ruta/` por tus datos reales.
5. Pega el prompt y pulsa Enter. Claude genera el dashboard web interactivo y el PDF ejecutivo en la misma carpeta.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP / CRM | Facturación por cliente | Pipeline comercial |
|---|---|---|
| **SAP Business One** | Informes de ventas → Analítica por cliente → Exportar | Módulo CRM → Oportunidades → Exportar |
| **Sage 50/200** | Clientes → Informes → Ventas por cliente y mes → CSV | Sage CRM → Oportunidades → Exportar |
| **A3 ERP** | Ventas → Informes → Facturación por cliente → Excel/CSV | Normalmente CRM externo |
| **Holded** | Ventas → Analítica → Por cliente → CSV | CRM Holded → Pipeline → Exportar |
| **Odoo** | Facturación → Análisis de ventas → Agrupar cliente/mes → CSV | CRM → Oportunidades → Exportar |
| **HubSpot / Pipedrive / Zoho** | — | Deals → Vista de pipeline → Exportar CSV |

Columnas mínimas en `facturacion_cliente.csv`: `cliente`, `mes`, `importe`. En `pipeline.csv`: `prospecto`, `estado`, `importe_estimado`, `probabilidad`.

> ⚠️ **Nota de sector:** diseñado para PYMEs de servicios, consultoría, agencias, despachos profesionales e industria B2B con carteras manejables (10-200 clientes activos) donde la concentración por cliente es un riesgo real. Si vendes B2C masivo (retail, ecommerce, hostelería), la concentración se mide distinto (por canal, categoría o producto) y este pack no aplica tal cual. Si además quieres anticipar qué cliente concreto puede marcharse, encadénalo con [caso-42 (alerta temprana de fuga de clientes)](../caso-42-alerta-temprana-fuga-clientes/) y [caso-34 (detección de churn)](../caso-34-deteccion-churn-clientes/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años de C-Suite. Trabajo con PYMEs de 1-50M€ en industria, mayoristas y construcción.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 Reserva 30 min: https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>concentración de clientes pyme, dependencia cliente grande b2b, índice HHI facturación, análisis riesgo cartera clientes, plan diversificación comercial pyme, cuántos clientes nuevos necesito para diversificar, impacto perder cliente principal ebitda, consultoría concentración ingresos, dashboard concentración clientes claude code, análisis top 3 clientes facturación</sub>
