# LÉEME — Caso 23: Rentabilidad real por canal

## El problema

Muchas PYMEs agroalimentarias (conserveras, distribuidoras, productoras) miden la rentabilidad de sus canales de venta solo por facturación bruta. Pero cuando descuentas logística, mermas, rappels, packaging especial y el coste financiero de cobrar a 90-120 días… el ranking cambia por completo.

El canal que más facturas puede ser el que menos margen neto te deja. Y eso te lleva a invertir recursos (comerciales, stock, capacidad de producción) en el canal equivocado.

## Qué contiene este ZIP

| Archivo | Qué es |
|---|---|
| `ventas_canal.csv` | Facturación por canal, producto y mes (Q1 2025) |
| `costes_logisticos.csv` | Costes de transporte, rappels, packaging y gestión por canal |
| `mermas.csv` | Pérdidas por devoluciones, roturas y rechazos por canal |
| `cobros_canal.csv` | Detalle de facturas con días reales de cobro por canal |
| `prompt.txt` | El prompt que pegas en Claude Code |
| `LEEME.md` | Este archivo |

## Cómo usarlo paso a paso

1. **Instala Claude Code** si no lo tienes:
   ```
   npm install -g @anthropic-ai/claude-code
   ```

2. **Copia los 4 CSVs** a una carpeta de tu ordenador, por ejemplo:
   ```
   C:\Users\TU_USUARIO\Downloads\Ejemplo Claude Code\Vídeo 23\
   ```

3. **Abre una terminal** (CMD, PowerShell, iTerm, Terminal de Mac)

4. **Inicia Claude Code:**
   ```
   claude
   ```

5. **Abre `prompt.txt`**, copia el contenido y pégalo en Claude Code

6. **Antes de darle a Enter**, cambia estas variables:
   - `[EMPRESA]` → el nombre de tu empresa
   - `[MES AÑO]` → el periodo que quieras analizar (ej: "Q1 2025")
   - Las rutas `@"..."` → apúntalas a donde hayas guardado los CSVs

7. **Pulsa Enter** y deja que Claude Code trabaje. No toques nada.

## De dónde sacar tus propios datos

Para sustituir los CSVs de ejemplo por datos reales de tu empresa:

- **ventas_canal.csv** → Exporta desde tu ERP las ventas desglosadas por canal de venta, producto, mes e importe. En A3 (Informes > Ventas por canal), Sage (Listados > Ventas), Holded (Ventas > Exportar), SAP (VA05 o tabla VBAK), Odoo (Ventas > Informes > Análisis de ventas).

- **costes_logisticos.csv** → Los costes de transporte, rappels y packaging los encontrarás en contabilidad (cuentas 624, 629, 607). Si usas A3 o Sage, exporta el mayor de esas cuentas con desglose analítico por canal.

- **mermas.csv** → Revisa los albaranes de devolución y los partes de incidencias de almacén. En la mayoría de ERPs está en Almacén > Movimientos > Salidas por merma/devolución.

- **cobros_canal.csv** → Exporta el listado de efectos o facturas cobradas con fecha de emisión y fecha de cobro real. En A3 (Tesorería > Efectos cobrados), Sage (Gestión de cobros), Holded (Cobros > Exportar).

## Nota importante

Este prompt está diseñado para el **sector agroalimentario** (conserveras, productoras, distribuidoras de alimentación). Los conceptos de merma, rappel a gran distribución, costes de plataforma logística y plazos de cobro por canal son específicos de este sector.

Si tu empresa es de otro sector, el prompt funciona igualmente pero deberás adaptar los tipos de coste logístico y merma a tu realidad (ej: en construcción serían costes de transporte de obra, mermas de material, etc.).

---

Creado por Isaac Romà · https://isaacroma.com
