# Caso 30 · Forecast de tesorería a 90 días — Anticipa cualquier tensión de caja con semanas de margen

> **Resultado:** Dashboard interactivo + Excel + PDF que cruzan saldo bancario, cobros previstos y pagos comprometidos. Te dice exactamente qué día tu saldo se vuelve rojo y por qué, con tiempo para reaccionar.

## 🎯 Problema que resuelve

La mayoría de PYMEs españolas gestionan la tesorería a ojo: miran el saldo del banco cada semana y rezan para que las nóminas, el IVA, el IRPF y los pagos a proveedores no coincidan en una fecha mala. Cuando el gerente detecta la tensión ya es tarde: toca pedir favores al banco, renegociar vencimientos con proveedores clave o adelantar cobros con descuento, destruyendo margen y credibilidad. El problema no es la falta de rentabilidad, sino la falta de visibilidad: el P&L dice que la empresa gana dinero mientras la caja se tensiona porque nadie ha cruzado en una sola vista el saldo real por banco, las facturas emitidas con su DSO real (no el teórico), los pagos recurrentes (nóminas, SS, IVA, IRPF, alquileres) y los compromisos puntuales con proveedores. Este caso automatiza ese cruce día a día durante los próximos 90 días y genera tres entregables: una web local con dashboard navegable, un Excel con la proyección diaria y alertas, y un PDF ejecutivo con acciones concretas para evitar cada punto rojo (adelantar un cobro, aplazar un pago, mover fondos entre cuentas). Pasas de reaccionar a planificar.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `datos/saldo_bancario.csv` | Saldo actual por cuenta bancaria |
| `datos/facturas_pendientes.csv` | Facturas emitidas pendientes de cobro con vencimiento y DSO real |
| `datos/pagos_comprometidos.csv` | Nóminas, impuestos, alquileres y proveedores comprometidos |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_30_Forecast_Tesoreria\`) manteniendo la subcarpeta `datos/` tal cual.
3. **Abre la terminal** en la carpeta raíz y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md`, `prompt.txt` y los 3 CSVs** al chat para que la IA entienda el contexto antes de ejecutar.
5. **Edita `prompt.txt`** sustituyendo `[EMPRESA]`, `[MES AÑO]` y las rutas de los CSVs, pégalo en Claude Code y pulsa Enter. En minutos tendrás web local + Excel + PDF con el forecast a 90 días.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Saldo bancario | Facturas pendientes de cobro | Pagos comprometidos |
|---|---|---|---|
| **A3 ERP (Wolters Kluwer)** | Conciliación bancaria / Posición de bancos | Ventas → Informes → Vencimientos pendientes | Compras → Vencimientos pendientes de pago |
| **Sage 50 / Sage 200** | Tesorería → Posición bancaria | Clientes → Vencimientos → Cartera de cobros | Proveedores → Cartera de pagos |
| **Holded** | Tesorería → Cuentas bancarias | Ventas → Facturas → Filtro "Pendiente" | Compras → Facturas pendientes |
| **Odoo** | Contabilidad → Panel de tesorería | Contabilidad → Informes → Antigüedad deudores | Contabilidad → Informes → Antigüedad acreedores |
| **SAP Business One** | Finanzas → Posición de bancos | Informes financieros → Antigüedad de deudores | Informes financieros → Antigüedad de acreedores |
| **Contasol / ContaPlus** | Mayor de cuentas 572 | Vencimientos de clientes (430) | Vencimientos de proveedores (400) |

> ⚠️ **Nota de sector:** Diseñado para **servicios profesionales** (consultoras, asesorías, despachos, agencias) con facturación recurrente y pagos predecibles. Si tu empresa es **industria, mayoristas o construcción**, los conceptos de pago cambian: certificaciones de obra, pagos a 60/90 días, estacionalidad fuerte y liquidaciones de IVA más volátiles. El prompt sigue funcionando: adapta los conceptos recurrentes de `pagos_comprometidos.csv` a tu realidad (anticipos, retenciones, pagos a cuenta). Para rentabilidad real por cliente o referencia, complementa con [caso-28 (rentabilidad clientes asesoría)](../caso-28-rentabilidad-clientes-asesoria/) o [caso-29 (coste real gran distribución)](../caso-29-coste-real-gran-distribucion/).

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>forecast tesorería 90 días PYME, previsión cash flow automatizada, control liquidez empresa española, Claude Code para CFO, DSO real cobros clientes, calendario pagos nóminas IVA IRPF, dashboard tesorería interactivo, evitar tensión caja PYME, automatización CFO con IA, consultoría financiera PYMEs industriales España</sub>
