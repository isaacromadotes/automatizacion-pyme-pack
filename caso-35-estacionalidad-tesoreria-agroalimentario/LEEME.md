# Caso 35 — Estacionalidad destroza la tesorería

## El problema

En agroalimentario (conservas, aceite, vino, frutos secos, hortofrutícola) la caja es un yoyó. En campaña pagas materia prima, mano de obra y energía a toda máquina. Fuera de campaña te sobra tesorería y nadie se acuerda del drama. Cada año, la misma sorpresa: septiembre llega, la póliza se tensa, el banco pide avales y el gerente firma lo que le pongan delante.

El problema no es la estacionalidad. **El problema es llegar tarde a verla.**

## Qué resuelve este prompt

Conecta producción, ventas, cobros y pagos fijos → genera un forecast mensual de tesorería → identifica los meses de tensión (meses con saldo negativo) → calcula con cuántos días de antelación se puede anticipar → entrega:

- Una web con el gráfico anual + tabla mensual (localhost)
- Un Excel navegable con el forecast completo
- Un HTML dashboard para presentar al banco

Resultado típico: la póliza baja de 120K€ a 60K€ porque vas con datos, no con prisas.

## Qué contiene este ZIP

- `LEEME.md` — este archivo
- `prompt.txt` — el prompt para pegar en Claude Code
- `csvs/produccion_anual.csv` — costes mensuales de producción (MP, MOD, energía, otros)
- `csvs/ventas_previstas.csv` — ventas previstas por canal
- `csvs/cobros_previstos.csv` — DSO medio por canal (días hasta cobro)
- `csvs/pagos_fijos.csv` — pagos recurrentes mensuales

## Cómo usarlo (paso a paso)

1. **Instala Claude Code** → https://docs.claude.com/en/docs/claude-code/overview
2. **Copia esta carpeta completa** a una ruta de tu equipo (por ejemplo `C:\Casos\caso_35` o `~/Casos/caso_35`)
3. **Abre la terminal** en esa carpeta y ejecuta: `claude`
4. **Arrastra `LEEME.md` y `prompt.txt` a la ventana de Claude Code** (así entiende el contexto antes de ejecutar)
5. **Pega el prompt** de `prompt.txt`
6. **Cambia las variables entre corchetes**: `[EMPRESA]`, `[MES AÑO]`, y las rutas `@csvs/*.csv`
7. **Enter** y espera. Claude Code generará web + Excel + HTML.

## De dónde sacar tus datos reales (ERP)

Reemplaza los CSVs de ejemplo con exports de tu ERP:

| Dato | Dónde está en tu ERP |
|---|---|
| Costes de producción mensuales | **A3 / Sage 50 / Sage 200**: módulo de Contabilidad → Mayor por centro de coste. **Holded**: Contabilidad → Informes → Pérdidas y Ganancias por mes. **SAP B1**: Finanzas → Informes financieros → P&G por período. **Odoo**: Contabilidad → Informes → P&G con desglose mensual. **Navision/BC**: Cuentas de resultados → Export a Excel. |
| Ventas previstas por canal | CRM o módulo comercial. **Odoo CRM / HubSpot / Pipedrive**: pipeline por mes y canal. Si no tienes CRM, exporta facturación del año anterior y ajusta a mano. |
| DSO medio por canal | **A3 / Sage**: informe de antigüedad de saldos por cliente, agrupado por canal/segmento. Si no tienes el dato limpio, usa: gran distribución 60-90 días, horeca 30-45 días, exportación 90-120 días. |
| Pagos fijos recurrentes | Mayor contable de las cuentas 621, 622, 623, 628, 629 (alquileres, reparaciones, seguros, suministros). También cuotas de leasing y préstamos del cuadro de amortización. |

**Importante**: este prompt está diseñado para empresas con **estacionalidad marcada** (agroalimentario, turismo, retail navideño, construcción, educación). Si tu negocio es lineal, cámbialo por el caso de "forecast de tesorería a 13 semanas" (caso 12 de la serie).

---

Creado por Isaac Romà · https://isaacroma.com
