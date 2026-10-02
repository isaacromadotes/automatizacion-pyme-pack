# Caso 17 · Cierre mensual en 48h — Coste de producción real por referencia

> Pasa de **2 semanas** de cierre mensual manual a **48 horas**, con **alertas automáticas** de desviación de coste por referencia.

## 🎯 Problema que resuelve

En una PYME industrial con producción propia y varias referencias, el cierre mensual tarda dos semanas no porque el equipo sea lento sino porque calcular el coste real de cada producto es un infierno manual. Hay que cruzar escandallos con precios de compra actualizados materia prima a materia prima, repartir horas de mano de obra directa por línea y producto a partir de partes de operario, y distribuir los costes indirectos (luz, alquiler, mantenimiento, amortizaciones) entre 50, 80 o 200 referencias aplicando criterios de reparto que casi siempre viven en una hoja Excel aparte que solo el responsable de controlling entiende. Cuando por fin cierras ya han pasado 15 días del mes siguiente, el margen bruto por referencia llega tarde y no sabes qué producto ha subido de coste hasta que es demasiado tarde para repercutirlo en el PVP o renegociar con proveedor. Este pack automatiza el proceso entero: Claude Code cruza escandallos, precios de materia prima actuales y del mes anterior, horas de producción reales por referencia y costes indirectos con su criterio de reparto, calcula el coste unitario completo de cada referencia, compara contra el mes anterior y lanza alertas de desviación. Cierre en 48 horas con hoja de costes por referencia, informe HTML ejecutivo y alertas automáticas priorizadas por impacto.

## 📦 Archivos del pack

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Documento inicial con la explicación del caso. |
| `prompt.txt` | Prompt listo para pegar en Claude Code. |
| `escandallos.csv` | Recetas: materia prima y cantidad por referencia. |
| `precios_mp.csv` | Precios actuales y del mes anterior de cada materia prima. |
| `produccion_junio.csv` | Horas de producción, unidades fabricadas y coste hora MOD por referencia. |
| `indirectos_junio.csv` | Costes indirectos del mes con su criterio de reparto. |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la [documentación oficial](https://docs.anthropic.com/en/docs/claude-code): `npm install -g @anthropic-ai/claude-code`
2. **Descomprime este pack** en una carpeta local (ej. `C:\Cierre_Produccion\`) y abre la terminal dentro con el comando `claude`.
3. **Arrastra a la ventana de Claude Code** el `LEEME.md`, el `prompt.txt` y los 4 CSV para que tenga todo el contexto.
4. **Copia el contenido de `prompt.txt`**, pégalo en Claude Code y sustituye `[EMPRESA]` y `[MES AÑO]` por tus datos.
5. **Pulsa Enter**: en 3-5 minutos Claude Code calcula el coste unitario completo por referencia, levanta una web local con la hoja de costes y alertas de desviación, y genera el PDF ejecutivo del cierre.

## 🔌 Cómo exportar los datos desde tu ERP

| Dato | A3ERP | Sage 200 | Holded | SAP Business One / S/4HANA | Odoo | Contasol / ContaPlus |
|---|---|---|---|---|---|---|
| Escandallos / BOM | Fichas técnicas → Exportar | Producción → Escandallos → Exportar | Productos → Composición → Exportar | Transacción CS03 (BOM) → Exportar | Fabricación → Listas de materiales → Exportar | — (gestiona en módulo auxiliar) |
| Precios materia prima | Compras → Últimas facturas / PMP → Exportar | Compras → Precios proveedor → Exportar | Compras → Productos → Exportar | Compras → Lista de precios → Exportar | Compras → Tarifas de proveedor → Exportar | Mayor cuentas grupo 60 → Exportar |
| Producción del mes | Fabricación → Partes de producción → Exportar | Producción → Órdenes de fabricación → Exportar | Fabricación → Órdenes → Exportar | Producción → Confirmaciones de orden → Exportar | Fabricación → Órdenes de producción → Exportar | — |
| Costes indirectos | Contabilidad analítica (cuentas 62/65/68) | Contabilidad analítica → Exportar | Contabilidad → Cuentas de gasto → Exportar | Centros de coste → Exportar | Contabilidad analítica → Exportar | Mayor cuentas 62/65/68 → Exportar |

> ⚠️ **Nota de sector:** este pack está diseñado para **PYMEs con producción propia y varias referencias**: conserveras, alimentación, química, cosmética, plásticos, farmacéutica, envases, panificadoras, cárnicas, textil. Si tu negocio es servicios, distribución pura o construcción por obra, este caso no aplica. Para completar el circuito de cierre y control de margen, combina con el [caso-01 (cierre mensual)](../caso-01-cierre-mensual/) y el [caso-12 (desviaciones de proyectos)](../caso-12-desviaciones-proyectos/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años en C-Suite.
Ayudo a **PYMEs industriales, mayoristas y de construcción (1-50M€)** a automatizar operaciones y recuperar margen con IA aplicada al negocio real, no a la tecnología.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **Automatización a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min conmigo:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>coste de producción real por referencia, cierre mensual industrial 48 horas, escandallos automáticos pyme, cálculo coste unitario fabricación, reparto costes indirectos producción, alertas desviación coste producto, hoja de costes conservera, controlling industrial automatizado, bom materia prima mano de obra, coste producto conservera alimentación</sub>
