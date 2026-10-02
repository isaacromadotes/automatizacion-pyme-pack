# Caso 19 — Margen desconocido por producto

## El problema

Tu empresa vende 120 referencias pero no sabes cuáles generan margen real y cuáles solo mueven volumen. El producto estrella en ventas puede ser el peor en rentabilidad.

**Metalúrgica Pérez S.L.** factura millones en tornillería... con un 8% de margen. Mientras, la soldadura inox que apenas vende genera un 34%.

## Qué hay en este pack

| Archivo | Qué contiene |
|---------|-------------|
| `ventas_12m.csv` | Ventas mensuales de 10 referencias (12 meses) |
| `costes_referencia.csv` | Costes desglosados por referencia (material, mano de obra, logística) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |

## Cómo usarlo

1. Instala [Claude Code](https://docs.anthropic.com/en/docs/claude-code) si aún no lo tienes.
2. Copia los CSV a una carpeta local (ej: `C:\Users\TuUsuario\Analisis`).
3. Abre Claude Code en esa carpeta.
4. Pega el contenido de `prompt.txt` y pulsa Enter.
5. Claude analizará los datos y generará:
   - Ranking de rentabilidad por referencia
   - Informe HTML interactivo estilo KPMG (cuadrante volumen × margen)
   - Excel con dashboard siguiendo estilo profesional
   - Alertas sobre productos con margen < 10%

## Adáptalo a tus datos reales

Sustituye los CSV de ejemplo por exportaciones de tu ERP:

| ERP | Dónde sacar los datos |
|-----|----------------------|
| **A3 ERP** | Informes > Ventas por artículo + Costes de producción |
| **Sage 200** | Comercial > Estadísticas de ventas + Fabricación > Costes |
| **Holded** | Ventas > Exportar facturas + Productos > Costes |
| **SAP Business One** | Informes financieros > Análisis de rentabilidad |
| **Odoo** | Ventas > Análisis + Fabricación > Costes de producto |

Mantén las mismas columnas de los CSV de ejemplo.

## Sector

Este caso está pensado para **industria y distribución** (metalurgia, ferretería industrial, suministros), pero aplica a cualquier negocio con catálogo de productos y costes variables.

---

Creado por **Isaac Romà** · [isaacroma.com](https://isaacroma.com)
