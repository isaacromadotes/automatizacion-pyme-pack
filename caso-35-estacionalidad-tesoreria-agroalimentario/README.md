# Caso 35 · Estacionalidad destroza la tesorería — Forecast anual para agroalimentario y negocios de campaña

> **Resultado:** La póliza de crédito baja de 120K€ a 60K€ porque llegas al banco con datos, no con prisas. Forecast mensual de tesorería que anticipa meses de tensión con antelación suficiente para negociar.

## 🎯 Problema que resuelve

En agroalimentario (conservas, aceite, vino, frutos secos, hortofrutícola) la caja funciona como un yoyó anual. En campaña se paga materia prima, mano de obra extra y energía a plena carga mientras la facturación todavía no entra porque los grandes clientes cobran a 60, 90 o 120 días. Fuera de campaña sobra tesorería, nadie se acuerda del drama vivido y los excedentes se destinan a amortizar deuda, repartir dividendos o acometer inversiones sin reserva para la siguiente campaña. Cada año se repite la misma secuencia: septiembre llega, la póliza se tensa, el banco pide avales o garantías adicionales y el gerente firma lo que le ponen delante porque no tiene alternativa. El problema no es la estacionalidad en sí —es estructural del sector— sino llegar tarde a verla: cuando se detecta la tensión quedan 15 días para resolverla y las condiciones son leoninas, cuando con 90-120 días de margen se negocia una ampliación de póliza, un confirming adicional o un adelanto de cobros a coste razonable. Este caso cruza costes de producción mensualizados, ventas previstas por canal, DSO real por canal y pagos fijos recurrentes, genera un forecast mensual anual de tesorería, identifica los meses con saldo negativo y entrega tres salidas: web local con gráfico anual y tabla mensual, Excel navegable con el forecast completo y dashboard HTML listo para presentar al banco con cifras y escenarios.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `csvs/produccion_anual.csv` | Costes mensuales de producción (MP, MOD, energía, otros) |
| `csvs/ventas_previstas.csv` | Ventas previstas por canal |
| `csvs/cobros_previstos.csv` | DSO medio por canal (días hasta cobro) |
| `csvs/pagos_fijos.csv` | Pagos recurrentes mensuales |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_35_Estacionalidad\`) manteniendo la subcarpeta `csvs/` tal cual.
3. **Abre la terminal** en la carpeta raíz y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md` y `prompt.txt`** al chat para dar contexto antes de ejecutar.
5. **Edita `prompt.txt`** cambiando `[EMPRESA]`, `[MES AÑO]` y las rutas `@csvs/*.csv`, pégalo y pulsa Enter. Obtendrás web local + Excel + dashboard HTML con el forecast anual.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Costes producción mensuales | Ventas previstas por canal | DSO por canal | Pagos fijos recurrentes |
|---|---|---|---|---|
| **A3 ERP (Wolters Kluwer)** | Mayor por centro de coste | Módulo comercial / Histórico | Antigüedad saldos por cliente | Mayor cuentas 621-629 |
| **Sage 50 / Sage 200** | P&L por centro de coste mensual | Previsión comercial | Antigüedad saldos agrupada | Mayor contable + leasing |
| **Holded** | Contabilidad → P&L mensual | Facturación recurrente / Pipeline | Informe antigüedad clientes | Gastos recurrentes |
| **SAP Business One** | Finanzas → P&L por período | Oportunidades CRM / Histórico | Antigüedad deudores | Pagos recurrentes |
| **Odoo** | Contabilidad → P&L con desglose | CRM → Pipeline por mes | Antigüedad deudores | Contabilidad → Gastos recurrentes |
| **Navision / Business Central** | Cuentas de resultados → Export | Previsión ventas | Antigüedad saldos | Mayor contable + cuadros amortización |
| **Contasol / ContaPlus** | Mayor por cuentas 6 | Facturación histórica | Vencimientos clientes (430) | Mayor cuentas 621-629 + leasing |

Si no tienes DSO limpio: usa gran distribución 60-90 días, HORECA 30-45 días, exportación 90-120 días como primera aproximación.

> ⚠️ **Nota de sector:** Diseñado para empresas con **estacionalidad marcada**: agroalimentario (conservas, aceite, vino, frutos secos, hortofrutícola), turismo, retail navideño, construcción con picos de campaña, educación con calendario escolar. Si tu negocio es lineal sin picos, usa [caso-30 (forecast tesorería 90 días)](../caso-30-forecast-tesoreria-90-dias/) para servicios profesionales o [caso-32 (forecast tesorería mayorista)](../caso-32-forecast-tesoreria-mayorista/) para distribución. Para enlazar con rentabilidad por SKU en gran distribución, combina con [caso-29 (coste real por referencia)](../caso-29-coste-real-gran-distribucion/).

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>forecast tesorería estacional agroalimentario, previsión caja anual conservas aceite vino, negociación póliza crédito campaña, Claude Code tesorería estacional, DSO gran distribución HORECA exportación, dashboard banco PYME agroalimentaria, automatización CFO industria conservera, tensión caja campaña agrícola, previsión financiera hortofrutícola, consultoría financiera PYME agroalimentaria España</sub>
