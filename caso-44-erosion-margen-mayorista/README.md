# Caso 44 · El margen se comprime y no sabes por qué — Waterfall de erosión de margen bruto en mayoristas

> **Resultado:** Descompone los 4,2 puntos de margen perdidos en 24 meses y los atribuye con precisión a coste de compra, descuentos, logística y devoluciones. Cada punto recuperado en un mayorista de 5M€ = 50.000 €/año directos al EBITDA.

## 🎯 Problema que resuelve

En mayoristas y distribuidores PYME españoles se repite la misma secuencia año tras año: la facturación se mantiene o incluso crece ligeramente, pero cada cierre entrega menos EBITDA que el anterior. El margen bruto se ha comprimido entre 3 y 5 puntos en los últimos 24 meses y nadie en la empresa puede decir con precisión por qué, porque la erosión no viene de una sola causa sino de cuatro frentes que actúan a la vez y que, cuando se miran agregados en el P&L, se cancelan mutuamente en el discurso: el coste de compra sube porque los proveedores repercuten inflación (parcialmente inevitable pero medible), los descuentos comerciales crecen porque el comercial responde a presión competitiva sin política escrita (evitable con disciplina), el coste logístico sube por combustible, última milla, almacén saturado y transportistas renegociando (corregible operativamente) y las devoluciones aumentan por errores de picking, pedidos mal servidos o calidad desigual del proveedor (corregible con proceso). Mezclar las cuatro causas en una sola cifra de "margen bruto" impide atajar ninguna, mientras cada punto perdido en un mayorista de 5M€ son 50.000€/año que no vuelven al EBITDA. Este caso automatiza el análisis en formato waterfall sobre 24 meses de datos cruzando ventas por familia con costes de compra, descuentos aplicados por motivo, costes logísticos prorrateados y devoluciones por causa raíz, atribuye cada décima de margen perdida a la causa concreta, clasifica cada bloque como inevitable / evitable / corregible y entrega un plan de acción priorizado con impacto estimado en EBITDA por línea de intervención.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `ventas_24m.csv` | 24 meses de ventas por familia con coste compra, descuentos, logística y devoluciones |
| `clientes.csv` | Maestro de clientes con tipología (instalador, constructora, obra pública) |
| `proveedores.csv` | Maestro de proveedores con familia que suministran |
| `descuentos_detalle.csv` | Descuentos aplicados por cliente y motivo |
| `devoluciones_detalle.csv` | Devoluciones con motivo (defectuoso, mal pedido, retraso) |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code` (requiere Node.js 18+).
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_44_Erosion_Margen\`) con los 5 CSVs en la raíz.
3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md`, `prompt.txt` y los 5 CSVs** al chat para dar contexto antes de ejecutar.
5. **Edita `prompt.txt`** cambiando `[EMPRESA]` y `[MES AÑO]` (deja `@./` como ruta), pégalo y pulsa Enter. Se abrirá dashboard HTML con waterfall de erosión, atribución por causa y plan de acción cuantificado.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Ventas por familia | Costes compra | Descuentos | Logística | Devoluciones |
|---|---|---|---|---|---|
| **SAP Business One** | OINV + INV1 (query) | OPOR + POR1 | Campo DiscPrcnt líneas | Cuenta 624 | Documentos AR Credit Memo |
| **A3 ERP / A3CON (Wolters Kluwer)** | Ventas por familia → Export | Compras por artículo | Descuentos en líneas factura | Costes generales (prorrateo) | Abonos (AB) |
| **Sage 50 / Sage 200** | Consulta MovLinA | Consulta MovLinC | Campo Descuento1 líneas | Cuenta 624 transportes | Docs tipo AB abonos |
| **Holded** | Analytics → Facturación | Inventario → Valoración stock | Facturación → Descuentos | Cuenta 624 | Facturas rectificativas |
| **Odoo** | Ventas → Analítica por familia | Compras → Analítica | Descuentos líneas | Analítica cuenta transporte | Abonos cliente |
| **Navision / Business Central** | Analítica dimensiones | Compras por artículo | Descuentos líneas | Cuenta transportes | Devoluciones de ventas |
| **Contasol / ContaPlus** | Facturación emitida grupo 70 | Compras grupo 60 | Rappels y descuentos grupo 706 | Cuenta 624 | Devoluciones 708 |

> ⚠️ **Nota de sector:** Diseñado específicamente para **mayoristas y distribuidores** (1-50M€, márgenes brutos 15-30%, muchos clientes B2B, múltiples familias). Para **fabricantes** la causa principal pasa a ser *coste de materias primas* en vez de *coste de compra* → avísalo al prompt. Para **retail/tienda física** añade *mermas* como quinta causa de erosión. Para **servicios profesionales** este caso no aplica → usa [caso-40 (rentabilidad por tipo servicio)](../caso-40-rentabilidad-por-tipo-servicio/). Para enlazar erosión de margen con tensión de caja, combina con [caso-32 (forecast tesorería mayorista)](../caso-32-forecast-tesoreria-mayorista/); para bajar al detalle de referencia dentro de las familias problemáticas, con [caso-29 (coste real por referencia)](../caso-29-coste-real-gran-distribucion/).

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>erosión margen bruto mayorista, waterfall margen distribución PYME, atribución causa margen perdido, política descuentos comercial, coste logístico última milla, devoluciones defectuoso mal pedido, Claude Code análisis margen EBITDA, renegociación proveedores escalados, suministros fontanería electricidad climatización, consultoría financiera mayoristas distribución España</sub>
