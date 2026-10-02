# Caso 26 · Visibilidad comercial multidimensional — Vendedor × Zona × Familia

> Deja de premiar al que más factura: identifica al que más margen deja, qué zona rinde y qué familia tira del P&L.

## 🎯 Problema que resuelve

En una PYME mayorista, distribuidora o industrial con red comercial, el único ranking que llega a dirección cada mes es el de facturación por vendedor. Y es un ranking tramposo: premia al que más mueve volumen, no al que más margen deja. El vendedor estrella de la cartelera puede estar vendiendo a descuentos agresivos a cuentas grandes con portes caros y DSO de 90 días, destruyendo margen; mientras el "mediano" del equipo trabaja referencias de familia premium en zonas rentables y aporta más resultado neto a la cuenta de resultados. Sin cruzar las tres dimensiones (vendedor, zona y familia de producto) a la vez, dirección no ve dónde se gana dinero de verdad: se mantienen zonas que consumen más coste comercial del que generan, se potencian familias que erosionan margen porque son las que piden los clientes grandes, y se incentiva al equipo con bonos sobre facturación en vez de sobre margen. Multiplicado por un año, son decenas de miles de euros de margen cedidos y una política comercial que corre en dirección contraria al P&L. Este pack genera un dashboard comercial multidimensional cruzando vendedor × zona × familia con los objetivos de cada comercial, calcula desviaciones sobre objetivo de facturación y de margen, lanza alertas automáticas (vendedor por debajo de margen objetivo, zona en pérdida, familia erosionando margen global) y entrega una presentación ejecutiva web lista para comité de dirección y una hoja Excel detallada para que el responsable comercial opere con ella.

## 📦 Archivos del pack

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Documento inicial con la explicación del caso. |
| `prompt.txt` | Prompt listo para pegar en Claude Code. |
| `ventas_detalle.csv` | Datos de ventas de ejemplo: 6 vendedores × 4 zonas × 8 familias × 2 meses (columnas: fecha, vendedor, zona, familia, cliente, importe, coste, unidades). |
| `objetivos.csv` | Objetivos mensuales por vendedor y margen esperado (columnas: vendedor, zona_principal, objetivo_mensual, objetivo_margen_pct). |
| `instrucciones_para_crear_tabla_excel.txt` | Guía de diseño del Excel (paleta, layout, tipografía). |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la [documentación oficial](https://docs.anthropic.com/en/docs/claude-code): `npm install -g @anthropic-ai/claude-code`
2. **Descomprime este pack** en una carpeta local (ej. `C:\Dashboard_Comercial\`) y abre la terminal dentro con el comando `claude`.
3. **Arrastra a la ventana de Claude Code** el `LEEME.md`, el `prompt.txt`, los 2 CSV y el `instrucciones_para_crear_tabla_excel.txt`.
4. **Copia el contenido de `prompt.txt`**, pégalo en Claude Code y sustituye `[EMPRESA]` y `[MES AÑO]` por tus datos (o déjalo con "Suministros Levante S.L." para probar).
5. **Pulsa Enter**: Claude Code genera el Excel detallado, la presentación web ejecutiva con alertas y abre el navegador.

## 🔌 Cómo exportar los datos desde tu ERP

| Dato | A3 / A3ERP | Sage 50/200 | Holded | SAP Business One | Odoo |
|---|---|---|---|---|---|
| Ventas detalladas (fecha, comercial, zona, familia, cliente, importe, coste, unidades) | Ventas → Albaranes/Facturas → Exportar con esas columnas | Informes → Ventas por representante / familia → Exportar | Ventas → Facturas → Filtros avanzados → Exportar CSV | Informes de ventas → Analysis by Sales Employee + Items List | Ventas → Informes → Análisis de ventas → Exportar |
| Objetivos por vendedor (facturación y margen) | Módulo comercial → Objetivos → Exportar | Objetivos de ventas → Exportar | Exportar manualmente del cuadro de objetivos | HR / Comisiones → Objetivos → Exportar | CRM → Objetivos de ventas → Exportar |

> ⚠️ **Nota de sector:** este pack está diseñado para empresas con **equipo comercial estructurado** (vendedores asignados a zonas y familias): mayoristas, distribución, industria con red comercial, seguros, inmobiliaria. Si tu equipo no está organizado por zona o familia, el dashboard funciona igual pero las conclusiones pierden fuerza; en ese caso conviene empezar por definir la segmentación. Para completar el análisis de rentabilidad, combina con el [caso-06 (rentabilidad clientes)](../caso-06-rentabilidad-clientes/), el [caso-19 (margen por producto)](../caso-19-margen-producto/) y el [caso-23 (rentabilidad por canal)](../caso-23-rentabilidad-canal/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años en C-Suite.
Ayudo a **PYMEs industriales, mayoristas y de construcción (1-50M€)** a automatizar operaciones y recuperar margen con IA aplicada al negocio real, no a la tecnología.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min conmigo:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>dashboard comercial multidimensional pyme, análisis vendedor zona familia producto, margen por comercial vs facturación, visibilidad comercial mayorista distribución, incentivar comercial por margen no facturación, alertas desviación objetivo comercial, rentabilidad por zona comercial pyme, cuadro de mando ventas vendedor zona, política comercial basada en margen, kpis comerciales mayorista industrial</sub>
