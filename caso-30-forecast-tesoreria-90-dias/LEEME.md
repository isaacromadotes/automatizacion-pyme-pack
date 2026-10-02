# Caso 30 — Forecast de tesorería a 90 días

## El problema que resuelve

¿Tendrás liquidez el mes que viene? Si tu respuesta es "creo que sí", tienes un problema.

La mayoría de PYMEs españolas gestionan la tesorería a ojo: miran el saldo del banco cada semana y rezan para que las nóminas, el IVA y los pagos a proveedores no coincidan en una fecha mala. Cuando descubren la tensión, ya es tarde.

Este pack te permite anticipar esa tensión **con semanas de margen**. Cruza tu saldo actual con todo lo que vas a cobrar y todo lo que vas a pagar, y te dice exactamente qué día tu saldo se vuelve rojo y por qué.

## Qué contiene este ZIP

- **LEEME.md** — Este archivo. Lo que estás leyendo.
- **prompt.txt** — El prompt que pegarás en Claude Code.
- **datos/saldo_bancario.csv** — Saldo actual por cuenta bancaria.
- **datos/facturas_pendientes.csv** — Facturas emitidas pendientes de cobro, con vencimiento y DSO real.
- **datos/pagos_comprometidos.csv** — Nóminas, impuestos, alquileres y proveedores comprometidos.

## Cómo usarlo paso a paso

1. **Instala Claude Code.** Si aún no lo tienes: [claude.com/claude-code](https://claude.com/claude-code).
2. **Descomprime este ZIP** en una carpeta de tu ordenador (por ejemplo `C:\Users\TuNombre\Downloads\Caso 30`).
3. **Abre tu terminal** (iTerm en Mac, PowerShell en Windows) y escribe `claude`.
4. **Arrastra `LEEME.md` y `prompt.txt`** a la ventana de Claude Code junto con los 3 CSVs. Esto da a Claude el contexto completo antes de ejecutar.
5. **Abre `prompt.txt`**, cambia las variables entre corchetes (`[EMPRESA]`, `[MES AÑO]`, ruta de los CSVs) por los tuyos, cópialo y pégalo en Claude Code.
6. **Pulsa Enter.** Claude Code generará:
   - Una **web local** con dashboard interactivo del forecast a 90 días.
   - Un **Excel** con la proyección diaria + gráfico + alertas.
   - Un **PDF** resumen con las acciones recomendadas para evitar la tensión.

## De dónde sacar estos datos en tu ERP

- **saldo_bancario.csv** → Extracto bancario del día (BBVA, Sabadell, Santander, CaixaBank). También desde la pasarela de tu ERP si tiene conciliación bancaria (A3, Sage 50, Holded, Odoo).
- **facturas_pendientes.csv** → Informe "Facturas pendientes de cobro" o "Antigüedad de saldos de clientes" de tu ERP:
  - **A3ERP** → Ventas · Informes · Vencimientos pendientes
  - **Sage 50** → Clientes · Vencimientos · Cartera de cobros
  - **Holded** → Ventas · Facturas · Filtrar por "Pendiente"
  - **Odoo** → Contabilidad · Informes · Antigüedad de saldos de clientes
  - **SAP Business One** → Informes financieros · Antigüedad de deudores
- **pagos_comprometidos.csv** → Mezcla de 3 fuentes:
  - Nóminas y SS → Tu asesoría laboral o módulo de RRHH
  - Impuestos (IVA, IRPF, IS) → Calendario fiscal de la AEAT + tu asesor
  - Proveedores → "Vencimientos pendientes de pago" del ERP

## Nota importante

Este prompt está diseñado para **servicios profesionales** (consultoras, asesorías, despachos, agencias) con facturación recurrente mes a mes y pagos predecibles. Si tu empresa es industria, comercio o construcción, los conceptos de pago cambian (certificaciones de obra, pagos a proveedores a 60/90 días, estacionalidad). El prompt sigue siendo válido pero conviene adaptar los conceptos recurrentes de `pagos_comprometidos.csv` a tu realidad.

El dato clave de la demo con la empresa ficticia **Consulting Horizonte S.L.** (1,8M€): el 22 de agosto el saldo cae a -8.400€ porque coinciden nóminas, pago a proveedor Z y liquidación de IVA. Con 22 días de margen, se puede adelantar el cobro de la factura F-2026-041 (Grupo Alaris, 12.300€) y aplazar el pago al proveedor Z (3.200€). Tensión evitada.

---

Creado por Isaac Romà · https://isaacroma.com
