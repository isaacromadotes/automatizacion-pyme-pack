# Caso 23 · Rentabilidad real por canal de venta — Agroalimentario

> El canal que más facturas suele ser el que menos margen neto deja. Descuenta logística, mermas, rappels, packaging y coste financiero del cobro: el ranking cambia por completo.

## 🎯 Problema que resuelve

En una PYME agroalimentaria (conservera, productora, distribuidora) la cuenta de resultados global sale, pero la rentabilidad por canal de venta es una caja negra. Se mide por facturación bruta porque es el único dato limpio que entrega el ERP, y a partir de ahí se decide a ciegas: dónde poner comerciales, qué canal priorizar en producción, a quién subir precio y a quién mimar. El problema es que la facturación bruta esconde cuatro bloques de coste que cambian radicalmente el margen neto por canal. Primero, la logística: HORECA pide entregas pequeñas y frecuentes, retail acepta palé completo, gran distribución exige plataforma propia con huecos horarios cerrados y penalizaciones por retraso. Segundo, los rappels y promociones negociadas con gran distribución, que se devengan contablemente a fin de año pero que ya están comprometidos. Tercero, las mermas por devolución, rotura y rechazo en recepción, que son enormes en gran distribución (controles de calidad estrictos) y mínimas en venta directa. Cuarto, el coste financiero del DSO: cobrar a 30 días no es lo mismo que cobrar a 120, y la diferencia a tipo medio bancario pesa. Este pack cruza ventas por canal, costes logísticos, mermas y cobros reales con fecha efectiva, calcula el margen neto por canal una vez descontados los cuatro bloques y entrega un ranking real de rentabilidad por canal con el impacto desglosado de cada partida. Decisiones comerciales y de capacidad basadas en margen neto, no en facturación.

## 📦 Archivos del pack

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Documento inicial con la explicación del caso. |
| `prompt.txt` | Prompt listo para pegar en Claude Code. |
| `ventas_canal.csv` | Facturación por canal, producto y mes (Q1 2025). |
| `costes_logisticos.csv` | Transporte, rappels, packaging y gestión por canal. |
| `mermas.csv` | Pérdidas por devoluciones, roturas y rechazos por canal. |
| `cobros_canal.csv` | Detalle de facturas con días reales de cobro por canal. |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la [documentación oficial](https://docs.anthropic.com/en/docs/claude-code): `npm install -g @anthropic-ai/claude-code`
2. **Descomprime este pack** en una carpeta local (ej. `C:\Rentabilidad_Canal\`) y abre la terminal dentro con el comando `claude`.
3. **Arrastra a la ventana de Claude Code** el `LEEME.md`, el `prompt.txt` y los 4 CSV para que tenga todo el contexto.
4. **Copia el contenido de `prompt.txt`**, pégalo en Claude Code y sustituye `[EMPRESA]`, `[MES AÑO]` y las rutas `@"..."` por tus datos reales.
5. **Pulsa Enter**: Claude Code calcula el margen neto por canal descontando logística, rappels, mermas y coste financiero del DSO, y entrega el ranking real con el desglose del impacto de cada partida.

## 🔌 Cómo exportar los datos desde tu ERP

| Dato | A3ERP | Sage 50/200 | Holded | SAP Business One | Odoo |
|---|---|---|---|---|---|
| Ventas por canal, producto y mes | Informes → Ventas por canal → Exportar | Listados → Ventas → Exportar | Ventas → Exportar | VA05 / tabla VBAK → Exportar | Ventas → Informes → Análisis de ventas |
| Costes logísticos (cuentas 624, 629, 607) | Mayor cuentas analíticas por canal → Exportar | Mayor cuentas 624/629/607 → Exportar | Contabilidad → Cuentas de gasto → Exportar | Centros de coste → Exportar | Contabilidad analítica → Exportar |
| Mermas, devoluciones y rechazos | Almacén → Movimientos → Salidas por merma/devolución | Almacén → Devoluciones → Exportar | Inventario → Movimientos → Exportar | Inventario → Devoluciones de clientes | Inventario → Albaranes de devolución |
| Cobros con fecha real por canal | Tesorería → Efectos cobrados → Exportar | Gestión de cobros → Exportar | Cobros → Exportar | Pagos recibidos → Exportar | Contabilidad → Pagos → Exportar |

> ⚠️ **Nota de sector:** este pack está diseñado para **PYMEs agroalimentarias** (conserveras, productoras, distribuidoras de alimentación) donde los conceptos de rappel a gran distribución, merma por rechazo en recepción, coste de plataforma logística y DSO por canal son específicos del sector. Funciona en otros sectores adaptando las partidas de coste logístico y merma a tu realidad (en construcción: transporte de obra y mermas de material; en industria: transporte propio y rechazo de calidad). Para completar el análisis de margen, combina con el [caso-06 (rentabilidad clientes)](../caso-06-rentabilidad-clientes/), el [caso-14 (rentabilidad real cliente)](../caso-14-rentabilidad-real-cliente/) y el [caso-19 (margen por producto)](../caso-19-margen-producto/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años en C-Suite.
Ayudo a **PYMEs industriales, mayoristas y de construcción (1-50M€)** a automatizar operaciones y recuperar margen con IA aplicada al negocio real, no a la tecnología.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min conmigo:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>rentabilidad real por canal de venta, margen neto canal horeca retail gran distribución, rappels gran distribución impacto margen, coste logístico por canal agroalimentario, dso canal cobro conservera, mermas rechazos devoluciones canal, análisis canal conservera productora, ranking rentabilidad canales distribuidora, margen por canal alimentación pyme, decisiones comerciales canal agroalimentario</sub>
