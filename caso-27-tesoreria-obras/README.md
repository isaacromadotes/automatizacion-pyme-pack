# Caso 27 · Tesorería separada por obra — Detecta qué obra genera caja y cuál la drena

> Varias obras simultáneas, una sola cuenta y el consolidado que parece sano: una obra buena puede estar financiando a una mala sin que lo veas.

## 🎯 Problema que resuelve

En una constructora o promotora con varias obras abiertas al mismo tiempo, la tesorería se mezcla en una única cuenta corriente y el saldo global parece razonable mes a mes. El problema aparece cuando se pregunta la pregunta correcta: ¿qué obra está generando caja y cuál la está drenando? Nadie lo sabe de verdad porque los cobros entran agregados, los pagos a subcontratas y proveedores salen igual, y lo único que llega a dirección es el extracto bancario de la empresa. En la práctica es muy habitual que una obra sana (con buena certificación mensual, cliente serio y plazos ajustados) esté financiando silenciosamente a otra obra con problemas (retrasos, extras no cobrados, cliente moroso) sin que nadie lo detecte hasta que la obra buena acaba, deja de aportar y aparece de golpe el agujero. Las decisiones de dirección sobre qué obras aceptar, qué plazos pactar, a qué cliente perseguir y dónde invertir margen comercial se toman a ciegas porque falta el dato básico: el flujo de caja real por obra. Este pack separa la tesorería obra por obra cruzando cobros, pagos y certificaciones pendientes de cobro, identifica cuáles obras drenan caja neta, cuáles están cubriendo a otras y cuánto riesgo hay concentrado en certificaciones pendientes, y entrega un panel ejecutivo web, un Excel operativo y un informe HTML profesional para dirección en minutos. Decisión informada obra a obra y aviso temprano cuando una obra empieza a convertirse en financiadora involuntaria del resto.

## 📦 Archivos del pack

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Documento inicial con la explicación del caso. |
| `prompt.txt` | Prompt listo para pegar en Claude Code. |
| `cobros_obra.csv` | Cobros reales de 4 obras (datos ficticios de ejemplo). |
| `pagos_obra.csv` | Pagos reales de las 4 obras. |
| `certificaciones_pendientes.csv` | Certificaciones emitidas pendientes de cobro. |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la [documentación oficial](https://docs.anthropic.com/en/docs/claude-code): `npm install -g @anthropic-ai/claude-code`
2. **Descomprime este pack** en una carpeta local (ej. `C:\Tesoreria_Obras\`) y abre la terminal dentro con el comando `claude`.
3. **Arrastra a la ventana de Claude Code** el `LEEME.md`, el `prompt.txt` y los 3 CSV para que tenga todo el contexto.
4. **Copia el contenido de `prompt.txt`**, pégalo en Claude Code y sustituye `[EMPRESA]`, `[MES AÑO]` y `[RUTA]` por tus datos reales.
5. **Pulsa Enter**: Claude Code separa la tesorería por obra, detecta drenajes y financiaciones cruzadas, y abre el panel web ejecutivo con el Excel y el informe HTML asociados.

## 🔌 Cómo exportar los datos desde tu ERP

| Dato | Sage 50/200 / A3 Innuva | Holded | SAP Business One | Odoo | Excel manual |
|---|---|---|---|---|---|
| Cobros por obra | Contabilidad → Extractos por centro de coste (obra = centro) | Proyectos → Cobros filtrados por proyecto → Exportar | WBS/PEP por obra → Flujo de caja por proyecto | Cuentas analíticas → Informe por obra | Extracto bancario con columna "obra" por movimiento |
| Pagos por obra | Contabilidad → Pagos por centro de coste → Exportar | Proyectos → Pagos por proyecto → Exportar | Flujo de caja por elemento PEP → Pagos | Cuentas analíticas → Pagos por obra | ídem (misma columna "obra") |
| Certificaciones emitidas pendientes de cobro | Cartera → Facturas emitidas pendientes por obra | Ventas → Pendiente de cobro por proyecto | Cartera clientes por elemento PEP | Facturas de cliente pendientes por analítica | Libro de certificaciones con estado |

> ⚠️ **Nota de sector:** este pack está diseñado para **constructoras y promotoras españolas con 2+ obras simultáneas**. Funciona igual para instaladoras con varios proyectos en paralelo, reformistas con 3+ clientes activos e industriales con pedidos grandes separados por centro de coste. No está pensado para empresas con una sola obra activa, servicios recurrentes sin imputación por cliente ni distribución mayorista. Requisito previo: tener imputación contable por obra (centros de coste o cuentas analíticas). Para completar el circuito económico de la obra, combina con el [caso-03 (control de obra)](../caso-03-control-obra/), el [caso-12 (desviaciones de proyectos)](../caso-12-desviaciones-proyectos/), el [caso-15 (certificaciones)](../caso-15-certificaciones-obra/) y el [caso-21 (extras de obra con firma)](../caso-21-extras-obra-firma/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años en C-Suite.
Ayudo a **PYMEs industriales, mayoristas y de construcción (1-50M€)** a automatizar operaciones y recuperar margen con IA aplicada al negocio real, no a la tecnología.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min conmigo:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>tesorería separada por obra constructora, cash flow por obra promotora, obras que drenan caja detectar, financiación cruzada entre obras, flujo de caja por centro de coste obra, panel tesorería obras simultáneas, imputación caja por proyecto construcción, cobros pagos certificaciones por obra, control financiero obra pyme construcción, dashboard tesorería promotora</sub>
