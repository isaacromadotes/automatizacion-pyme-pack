# Cierre mensual en 48 horas con Claude Code

## El problema

Tu cierre mensual tarda 10-15 días. Recopilar datos del ERP, consolidar costes por centro, cruzar con ventas, calcular márgenes... todo manual, todo lento. Tu competencia ya cierra en 48h.

## Qué hay dentro

| Archivo | Qué es |
|---|---|
| `prompt.txt` | Prompt listo para copiar y pegar en Claude Code |
| `balance_sumas_saldos.csv` | Balance de sumas y saldos — export típico de ERP |
| `costes_produccion.csv` | Costes por centro de coste (directos e indirectos) |
| `ventas_mes.csv` | Detalle de facturación del mes por cliente y pedido |

## Cómo usarlo

1. Instala Claude Code → https://docs.anthropic.com/en/docs/claude-code
2. Copia los 3 CSV en una carpeta de tu ordenador
3. Abre Claude Code, pega el contenido de `prompt.txt`
4. Cambia `[EMPRESA]` por el nombre de tu empresa, `[MES AÑO]` por el mes, y `@ruta/` por la ruta donde tengas los CSV
5. Pulsa Enter y deja que trabaje

## Datos de ejemplo

Los CSV contienen datos ficticios de "Metalúrgica Pérez" (agosto 2026). Úsalos para probar el prompt tal cual. Cuando funcione, sustituye por los exports reales de tu ERP.

### ¿De dónde saco estos CSV en mi ERP?

| Archivo | Dónde encontrarlo |
|---|---|
| `balance_sumas_saldos.csv` | Contabilidad → Balances → Sumas y Saldos → Exportar CSV |
| `costes_produccion.csv` | Producción / Contabilidad analítica → Costes por centro → Exportar |
| `ventas_mes.csv` | Ventas → Listado facturas emitidas del mes → Exportar |

Funciona con A3, Sage, Holded, Contaplus, SAP Business One, Odoo, y cualquier ERP que exporte CSV.

## Nota importante

Este prompt está diseñado para **empresas industriales y de fabricación** (centros de coste tipo corte, soldadura, pintura, montaje). Si tu empresa es de servicios, construcción o distribución, los centros de coste serán diferentes y necesitarás adaptar el prompt a tu estructura.

¿No sabes cómo adaptarlo? → https://calendly.com/asesor-online-ia/30min

---

Creado por Isaac Romà · https://isaacroma.com
