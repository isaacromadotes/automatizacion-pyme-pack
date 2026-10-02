# Caso 29 · Coste real por referencia para gran distribución — Deja de vender a pérdida a Mercadona, Carrefour o Lidl

> **Resultado:** Entre un 15% y un 25% de las referencias de un fabricante PYME se venden a pérdida real sin saberlo. Este caso te da la ficha de coste completa (producción + logística + merma + coste financiero) por referencia en una web interactiva.

## 🎯 Problema que resuelve

Mercadona, Carrefour, Lidl, Dia o Eroski piden una bajada del 3% y el gerente acepta porque "aún queda margen". Pero ese margen se calcula sobre un coste incompleto: la mayoría de fabricantes PYME suman solo materia prima, mano de obra y una parte de indirectos, dejando fuera la logística hasta plataforma, la merma por producto roto o rechazado y, sobre todo, el coste financiero de cobrar a 90 días —que en un entorno de tipos altos puede comerse 1-2 puntos de margen por referencia—. El resultado es un portfolio donde entre un 15% y un 25% de las SKUs se vende por debajo del coste real sin que nadie en el despacho de dirección lo sepa, mientras producción trabaja a tope y la caja se tensiona cada mes. Este caso cruza los cinco bloques de coste reales (producción, logística, merma, condiciones de cobro y precios de venta por canal) y devuelve una ficha de coste completa por referencia en una web interactiva local, identificando las SKUs deficitarias y el precio mínimo viable para cada negociación. Llegas a la mesa con el comercial de la cadena sabiendo exactamente hasta dónde puedes bajar sin perder dinero.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `datos_ejemplo/costes_produccion.csv` | Coste MP + MOD + indirectos por referencia |
| `datos_ejemplo/costes_logisticos.csv` | Transporte y manipulación por referencia |
| `datos_ejemplo/mermas.csv` | Tasa de merma por referencia y canal |
| `datos_ejemplo/condiciones_cobro.csv` | Plazos de pago y coste financiero |
| `datos_ejemplo/precios_venta.csv` | Precio de venta por referencia y canal |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_29_Coste_Real\`) manteniendo la subcarpeta `datos_ejemplo/` tal cual.
3. **Abre la terminal** en la carpeta raíz y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md` y `prompt.txt`** al chat para que la IA entienda el contexto antes de ejecutar.
5. **Pega el contenido de `prompt.txt`** y pulsa Enter. En ~2 minutos obtendrás una web local con la ficha de coste real de las 15 referencias de ejemplo. Para usarlo con tus datos, sustituye los 5 CSVs manteniendo nombres y columnas.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Costes producción | Mermas | Condiciones cobro / Precios venta |
|---|---|---|---|
| **SAP Business One** | Módulo CO-PC (Product Costing) / Escandallos | Tabla MARD de mermas | Condiciones comerciales por cliente / Tarifas de venta |
| **A3 ERP (Wolters Kluwer)** | Escandallos de fabricación | Regularizaciones de almacén | Condiciones de cobro cliente / Tarifas por canal |
| **Sage 200 / Sage X3** | Costes de artículos / BOM | Regularizaciones de almacén | Condiciones comerciales / Tarifas por canal |
| **Holded** | Productos → Coste de fabricación | Ajustes de inventario | Clientes → Formas de pago / Tarifas |
| **Odoo** | Fabricación → BOM + costes analíticos | Ajustes de inventario / rechazos | Condiciones de pago cliente / Listas de precios |
| **Contasol / ContaPlus** | No nativo (usa escandallo Excel paralelo) | Regularizaciones contables | Condiciones cliente / Facturación emitida |

> ⚠️ **Nota de sector:** Diseñado para **fabricantes alimentarios que venden a gran distribución** (Mercadona, Carrefour, Lidl, Dia, Eroski, Alcampo). Aplica con mínimos cambios a **fabricantes textiles** (El Corte Inglés, Primark, Inditex), **cosmética** (Druni, Primor) y **droguería/limpieza** vendiendo a supermercados. Las fórmulas de coste financiero y merma son universales; lo que cambia son los plazos de cobro típicos y las tasas de merma habituales por sector. Si no tienes los datos de logística o merma, es la primera señal de que estás negociando a ciegas: empieza por producción + estimación razonable del resto. Complementa con [caso-28 (rentabilidad real por cliente)](../caso-28-rentabilidad-clientes-asesoria/) si quieres aplicar la misma lógica a servicios recurrentes.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>coste real por referencia fabricante, negociación Mercadona Carrefour Lidl, margen real SKU gran distribución, ficha de coste completa alimentación, automatización control costes PYME industrial, Claude Code fabricantes alimentarios, coste financiero plazo cobro 90 días, merma logística gran distribución, escandallo SAP A3 ERP, consultoría automatización industria alimentaria España</sub>
