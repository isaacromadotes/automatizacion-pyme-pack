# Caso 32 · Forecast de tesorería a 90 días para mayoristas — Detecta tensiones de caja con 30+ días de margen

> **Resultado:** Suministros Levante S.L. (caso ficticio, mayorista) detecta un saldo de –23.000 € el 18 de agosto por coincidencia de nóminas + IVA + proveedor grande. **34 días de margen** para actuar antes de pedir favores al banco.

## 🎯 Problema que resuelve

La mayoría de mayoristas y distribuidoras españolas llevan la tesorería en un Excel que mira al pasado: saben lo que entró y lo que salió, pero no si tendrán caja dentro de 30, 60 o 90 días. El resultado es una tensión recurrente que llega con 3 días de margen en vez de 30, dependencia del banco en el peor momento (justo cuando el gerente huele la tensión, la línea de descuento se encarece) y decisiones de inversión, contratación o compra de stock tomadas a ciegas. El problema no es la rentabilidad sino la visibilidad: nadie cruza en una sola vista el saldo real por cuenta, los cobros pendientes por cliente con su DSO real, los pagos recurrentes (nóminas, SS, IVA, IRPF, alquileres, suministros) y los compromisos puntuales con proveedores grandes. En un mayorista con rotación alta y márgenes ajustados, bastan dos semanas de descuadre para quemar el margen anual de una familia de producto. Este caso automatiza el forecast diario a 90 días cruzando saldo bancario + cartera de cobros + cartera de pagos, genera una web interactiva local con el gráfico de evolución y marca en rojo cada día de tensión con el motivo exacto (qué pago entra, qué cobro falta, qué cuenta afecta). Pasas de reaccionar a planificar con un mes largo de antelación.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `saldo.csv` | Saldo bancario inicial por cuenta (datos ficticios) |
| `facturas_por_cobrar.csv` | Cobros pendientes de clientes con vencimientos |
| `pagos_previstos.csv` | Pagos comprometidos (nóminas, IVA, proveedores, fijos) |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code` (requiere Node.js 18+).
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_32_Forecast_Mayorista\`) con los 3 CSVs en la raíz.
3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md`, `prompt.txt` y los 3 CSVs** al chat para dar contexto antes de ejecutar.
5. **Edita `prompt.txt`** cambiando `[EMPRESA]` y `[MES AÑO]` (o déjalos para la demo), pégalo y pulsa Enter. Claude Code arrancará un servidor local; abre la URL que indique (normalmente `http://localhost:3000`).

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Saldo bancario | Cobros pendientes | Pagos previstos |
|---|---|---|---|
| **A3 ERP (Wolters Kluwer)** | Tesorería → Saldos bancarios | Cartera de cobros | Cartera de pagos |
| **Sage 50 / Sage 200** | Bancos → Posición | Clientes → Efectos a cobrar | Proveedores → Vencimientos |
| **Holded** | Tesorería → Cuentas | Facturas → Pendientes de cobro | Compras → Pendientes de pago |
| **SAP Business One** | Banca → Posición de caja | Cobros → Documentos abiertos | Pagos → Documentos abiertos |
| **Odoo** | Contabilidad → Panel bancos | Facturación → Facturas abiertas | Compras → Facturas de proveedor |
| **Contasol / ContaPlus** | Mayor cuenta 572 | Vencimientos de clientes (430) | Vencimientos de proveedores (400) |
| **FacturaScripts** | Tesorería → Cuentas | Recibos pendientes clientes | Recibos pendientes proveedores |

Exporta cada informe a CSV y renómbralos a `saldo.csv`, `facturas_por_cobrar.csv` y `pagos_previstos.csv`. Las columnas pueden variar — Claude Code se adapta.

> ⚠️ **Nota de sector:** Diseñado para **mayoristas, distribuidoras e industria** con flujos de caja recurrentes y predecibles. Si tu negocio es **estacional** (hostelería de temporada, retail navideño, agrícola de campaña), añade una línea al prompt indicando la estacionalidad para que el modelo ajuste picos y valles. Para servicios profesionales con cuota recurrente, es más adecuado [caso-30 (forecast tesorería 90 días servicios)](../caso-30-forecast-tesoreria-90-dias/). Para enlazar la tensión de caja con el margen real por producto, combina con [caso-29 (coste real por referencia)](../caso-29-coste-real-gran-distribucion/).

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>forecast tesorería mayorista 90 días, previsión cash flow distribución, control liquidez PYME mayorista, Claude Code tesorería ERP, DSO cobros clientes mayoristas, tensión caja nóminas IVA proveedor, dashboard tesorería interactivo, automatización CFO mayorista con IA, previsión caja Sage A3 Holded, consultoría financiera PYMEs distribución España</sub>
