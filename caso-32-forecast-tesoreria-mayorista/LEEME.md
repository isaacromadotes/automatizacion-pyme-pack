# Caso 32 — Forecast de tesorería a 90 días con Claude Code

## El problema que resuelve

La mayoría de PYMEs españolas llevan la tesorería en un Excel que **mira al pasado**: sabes lo que entró y lo que salió, pero no si tendrás caja dentro de 30, 60 o 90 días.

El resultado:
- Tensiones de liquidez que te pillan **con 3 días de margen** en vez de 30.
- Dependencia del banco en el peor momento (cuando ya hueles la tensión, la línea de descuento es más cara).
- Decisiones de inversión, contratación o compra **a ciegas**.

Este pack te permite montar un **forecast diario de tesorería a 90 días** cruzando tres fuentes: saldo actual, cobros pendientes y pagos comprometidos. Claude Code genera una web con el gráfico y marca en rojo los días con tensión.

**Caso de ejemplo (ficticio):** Suministros Levante S.L., mayorista. Detecta un saldo de –23.000€ el 18 de agosto por coincidencia de nóminas + IVA + proveedor grande. 34 días de margen para actuar.

---

## Qué contiene este ZIP

- `LEEME.md` — este archivo
- `prompt.txt` — el prompt que pegarás en Claude Code
- `saldo.csv` — saldo bancario inicial (datos ficticios)
- `facturas_por_cobrar.csv` — cobros pendientes de clientes
- `pagos_previstos.csv` — pagos comprometidos (nóminas, IVA, proveedores, fijos)

---

## Cómo usarlo paso a paso

1. **Instala Claude Code** (si no lo tienes):
   - Mac/Linux: `curl -fsSL https://claude.ai/install.sh | sh`
   - Windows: descarga el instalador oficial desde la web de Anthropic
   - Requiere Node.js 18 o superior

2. **Crea una carpeta** en tu PC, por ejemplo:
   `~/Descargas/Ejemplo Claude Code/`

3. **Copia los 3 CSVs** del ZIP a esa carpeta.

4. **Abre tu terminal** en esa carpeta y escribe: `claude`

5. **Arrastra `LEEME.md` y `prompt.txt`** a la ventana de Claude Code (para que entienda el contexto completo).

6. **Pega el contenido de `prompt.txt`** y pulsa Enter.

7. Cambia las variables **[EMPRESA]** y **[MES AÑO]** por los tuyos, o déjalos como vienen para la demo.

8. Claude Code generará el forecast, montará la web y arrancará el servidor. Abre el navegador en la URL que te indique (normalmente `http://localhost:3000`).

---

## De dónde sacar tus datos reales

Cuando quieras usarlo con los datos de tu empresa, estos son los informes que necesitas de tu ERP:

| ERP | Saldo bancario | Cobros pendientes | Pagos previstos |
|---|---|---|---|
| **A3 ERP** | Tesorería > Saldos bancarios | Cartera de cobros | Cartera de pagos |
| **Sage 50 / 200** | Bancos > Posición | Clientes > Efectos a cobrar | Proveedores > Vencimientos |
| **Holded** | Tesorería > Cuentas | Facturas > Pendientes de cobro | Compras > Pendientes de pago |
| **SAP Business One** | Banca > Posición de caja | Cobros > Documentos abiertos | Pagos > Documentos abiertos |
| **Odoo** | Contabilidad > Panel bancos | Facturación > Facturas abiertas | Compras > Facturas de proveedor |
| **FacturaScripts** | Tesorería > Cuentas | Recibos pendientes clientes | Recibos pendientes proveedores |

Exporta cada informe a CSV y renómbralos a `saldo.csv`, `facturas_por_cobrar.csv` y `pagos_previstos.csv`. Las columnas pueden variar — Claude Code se adapta.

---

## Nota importante

Este prompt está diseñado para **PYMEs del sector mayorista, industrial o distribución**, donde los flujos de caja son recurrentes y predecibles. Si tu negocio es estacional (hostelería de temporada, retail navideño, agrícola) añade al prompt una línea indicando la estacionalidad para que Claude Code ajuste el modelo.

Los datos de este ejemplo son **ficticios**. Cualquier parecido con empresas reales es casualidad.

---

Creado por Isaac Romà · https://isaacroma.com
