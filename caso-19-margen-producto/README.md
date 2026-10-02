# Caso 19 · Margen real por producto — Descubre qué referencias te hacen ganar dinero

> **Metalúrgica Pérez S.L.**: factura millones en tornillería con **8% de margen**, mientras la soldadura inox que apenas vende da el **34%**. El producto estrella en ventas suele ser el peor en rentabilidad.

## 🎯 Problema que resuelve

En una PYME industrial o de distribución con catálogo de 50-200 referencias, el ranking de ventas se mira cada semana pero el ranking de margen real casi nunca existe, y cuando se mira a ojo se mira mal: se usa el margen bruto de ficha ("este producto me da el 30%") sin descontar el coste real de mano de obra directa imputada ni el coste logístico asociado al tipo de referencia. El resultado es que la empresa cree que vive del producto A cuando en realidad vive del producto G, dedica fuerza comercial y rotación de almacén a las referencias que mueven volumen pero no dejan margen, y mantiene vivas referencias con margen negativo porque "siempre se han vendido". Multiplicado por 120 SKUs y 12 meses, hay decenas de miles de euros de margen desaprovechado y un catálogo inflado que encarece compras, almacén y gestión. Este pack cruza las ventas mensuales de los últimos 12 meses con los costes desglosados por referencia (material, mano de obra y logística) y genera un ranking de rentabilidad real por SKU, un informe HTML interactivo con cuadrante volumen × margen al estilo consultora, un Excel con dashboard profesional y alertas automáticas sobre referencias con margen bajo o negativo. Decisiones de catálogo, de precio y de foco comercial basadas en el margen real, no en la facturación.

## 📦 Archivos del pack

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Documento inicial con la explicación del caso. |
| `prompt.txt` | Prompt listo para pegar en Claude Code. |
| `ventas_12m.csv` | Ventas mensuales de 10 referencias durante 12 meses. |
| `costes_referencia.csv` | Costes desglosados por referencia (material, mano de obra, logística). |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la [documentación oficial](https://docs.anthropic.com/en/docs/claude-code): `npm install -g @anthropic-ai/claude-code`
2. **Descomprime este pack** en una carpeta local (ej. `C:\Analisis_Margen\`) y abre la terminal dentro con el comando `claude`.
3. **Arrastra a la ventana de Claude Code** el `LEEME.md`, el `prompt.txt` y los 2 CSV para que tenga todo el contexto.
4. **Copia el contenido de `prompt.txt`** y pégalo en Claude Code (ajusta nombre de empresa y periodo si quieres personalizarlo).
5. **Pulsa Enter**: Claude Code genera el ranking de rentabilidad por referencia, el informe HTML interactivo con cuadrante volumen × margen, el Excel con dashboard y las alertas de referencias con margen < 10%.

## 🔌 Cómo exportar los datos desde tu ERP

| Dato | A3ERP | Sage 200 | Holded | SAP Business One | Odoo |
|---|---|---|---|---|---|
| Ventas por artículo 12 meses | Informes → Ventas por artículo → Exportar | Comercial → Estadísticas de ventas → Exportar | Ventas → Exportar facturas por producto | Informes financieros → Ventas por artículo | Ventas → Análisis → Exportar |
| Costes por referencia (material, MOD, logística) | Fichas técnicas + Fabricación → Costes | Fabricación → Costes de producción → Exportar | Productos → Costes → Exportar | Análisis de rentabilidad → Exportar | Fabricación → Costes de producto → Exportar |

> ⚠️ **Nota de sector:** este pack está pensado para **industria ligera, metalurgia, ferretería industrial, suministros y distribución** con catálogo de productos físicos y costes variables identificables. Aplica a cualquier negocio con SKUs y márgenes por referencia. Para profundizar en el análisis de rentabilidad por cliente (otra dimensión complementaria), encadena con el [caso-06 (rentabilidad clientes)](../caso-06-rentabilidad-clientes/) y el [caso-14 (rentabilidad real cliente)](../caso-14-rentabilidad-real-cliente/); para análisis industrial de coste de producción completo, mira el [caso-17 (cierre de producción)](../caso-17-cierre-produccion/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años en C-Suite.
Ayudo a **PYMEs industriales, mayoristas y de construcción (1-50M€)** a automatizar operaciones y recuperar margen con IA aplicada al negocio real, no a la tecnología.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **Automatización a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min conmigo:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>margen real por producto pyme, ranking rentabilidad referencias industriales, análisis volumen vs margen sku, matriz bcg producto industrial, productos con margen negativo detectar, dashboard rentabilidad catálogo pyme, racionalizar catálogo productos industria, margen por referencia metalurgia, análisis abc rentabilidad sku, cuadro mando rentabilidad productos distribución</sub>
