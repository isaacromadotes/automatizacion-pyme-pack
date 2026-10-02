# CASO 17 · Cierre mensual en 48h: coste de producción automático

## El problema

Tu cierre mensual tarda 2 semanas. Y no es porque tu equipo sea lento — es porque calcular el **coste real de producción** de cada referencia (bote, unidad, producto) es un infierno manual:

- Materiales: cruzar escandallos con precios de compra actualizados
- Mano de obra directa: repartir horas de operarios por línea y producto
- Costes indirectos: repartir luz, alquiler, mantenimiento, amortizaciones… entre 50, 80, 200 referencias

Cuando por fin cierras, ya han pasado 15 días. Y no sabes qué producto ha subido de coste hasta que es demasiado tarde para reaccionar.

**Este pack automatiza todo el proceso. Cierre en 48 horas. Alertas de desviación por referencia.**

---

## Qué contiene este ZIP

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Este documento |
| `prompt.txt` | El prompt que pegarás en Claude Code |
| `escandallos.csv` | Recetas: qué materia prima lleva cada referencia y cuánta |
| `precios_mp.csv` | Precios actuales y del mes anterior de cada materia prima |
| `produccion_junio.csv` | Horas de producción, unidades fabricadas y coste hora MOD por referencia |
| `indirectos_junio.csv` | Costes indirectos del mes con su criterio de reparto |

Los datos son ficticios (una conservera mediterránea con 8 referencias) pero la estructura es la misma que necesitas en tu empresa.

---

## Cómo usarlo — 5 pasos

1. **Instala Claude Code** si aún no lo tienes: [claude.com/claude-code](https://claude.com/claude-code)
2. **Crea una carpeta** en tu ordenador (ej: `C:\Users\tu_usuario\Downloads\Ejemplo Claude Code\Vídeo 17`) y **copia dentro los 4 CSVs + este LEEME.md + el prompt.txt**.
3. **Abre Claude Code** en esa carpeta (terminal → `cd` a la carpeta → escribe `claude`).
4. **Arrastra** el `LEEME.md` y el `prompt.txt` a la ventana de Claude Code (para que entienda el contexto completo).
5. **Pega el contenido de `prompt.txt`** en el chat de Claude Code. Cambia las variables `[EMPRESA]` y `[MES AÑO]` por los tuyos. Pulsa Enter.

En 3-5 minutos tendrás una web local con la hoja de costes por referencia y alertas automáticas. Si el prompt está bien redactado, también un PDF ejecutivo.

---

## De dónde sacar TUS datos reales

Sustituye los CSVs de ejemplo por exports de tu ERP:

| Dato | Dónde encontrarlo |
|---|---|
| **Escandallos** | Módulo de fabricación / recetas. En **SAP** → Transacción CS03 (BOM). En **Odoo** → Fabricación → Listas de materiales. En **Sage 200** → Producción → Escandallos. En **A3ERP** → Fichas técnicas. En **Holded** → Productos → Composición. |
| **Precios materia prima** | Módulo de compras. Última factura de proveedor o precio medio ponderado del período. |
| **Producción del mes** | Módulo de fabricación / partes de producción. Horas reales imputadas a órdenes de fabricación. |
| **Costes indirectos** | Contabilidad analítica. Cuentas del grupo 62, 68 y 65 con criterio de reparto. |

Exporta cada uno a CSV manteniendo las mismas columnas que ves en los archivos de ejemplo. **No hace falta que sean idénticas**: Claude Code adapta el prompt a tu estructura, solo dile qué columna es cuál.

---

## Nota importante

Este prompt está diseñado para empresas **con producción propia y varias referencias**: conserveras, alimentación, química, cosmética, plásticos, farmacéutica, envases, panificadoras, cárnicas, textil.

Si tu negocio es **servicios**, **distribución pura** o **construcción por obra**, este caso NO es para ti — tengo otros vídeos de la serie orientados a esos sectores.

---

Creado por Isaac Romà · https://isaacroma.com
