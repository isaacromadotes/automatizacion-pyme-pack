# Caso 26 — Visibilidad comercial multidimensional

**Creado por Isaac Romà · https://isaacroma.com**

---

## El problema que resuelve

En una PYME mayorista (o cualquier empresa con equipo comercial), nadie sabe de verdad:

- Qué vendedor deja más margen (no el que más factura, el que más margen).
- Qué zona rinde mejor y cuál se come los recursos.
- Qué familia de producto tira del margen y cuál lo destruye.

El resultado: se incentiva a quien más vende aunque venda a pérdida, se mantienen zonas que no son rentables y se potencian familias de producto que están erosionando la cuenta de resultados.

Este pack genera un **dashboard comercial multidimensional** cruzando vendedor × zona × familia, con alertas automáticas y una presentación ejecutiva lista para dirección.

---

## Qué contiene este ZIP

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Este documento. |
| `prompt.txt` | El prompt que pegas en Claude Code. |
| `ventas_detalle.csv` | Datos de ventas de ejemplo (6 vendedores, 4 zonas, 8 familias, 2 meses). |
| `objetivos.csv` | Objetivos mensuales por vendedor y margen esperado. |
| `instrucciones_para_crear_tabla_excel.txt` | Guía de diseño del Excel (paleta, layout, tipografía). |

---

## Cómo usarlo (paso a paso)

1. **Instala Claude Code** (si aún no lo tienes): https://claude.com/claude-code
2. **Copia esta carpeta completa** a tu ordenador. Sugerido: `C:\Users\[tu usuario]\Downloads\Ejemplo Claude Code\Vídeo 26\`
3. **Abre la terminal** (iTerm en Mac, Terminal en Windows) en esa carpeta y escribe: `claude`
4. **Abre `prompt.txt`**, cópialo entero y pégalo en Claude Code.
5. **Cambia las variables** entre corchetes `[EMPRESA]`, `[MES AÑO]` por los datos reales (o déjalo como está para probar con la empresa ficticia Suministros Levante S.L.).
6. **Pulsa Enter** y espera. Claude Code generará el Excel, la presentación web ejecutiva y abrirá el navegador.

---

## De dónde sacas estos datos en tu ERP real

Según tu sistema, exporta a CSV lo siguiente:

| ERP | Dónde está |
|---|---|
| **A3 / A3ERP** | Ventas → Listado de albaranes/facturas → Exportar con columnas: fecha, comercial, zona, familia, cliente, importe, coste. |
| **Sage 50 / Sage 200** | Informes → Ventas por representante / familia → Exportar a Excel. |
| **Holded** | Ventas → Facturas → Filtros avanzados → Exportar CSV. |
| **SAP Business One** | Informes de ventas → "Analysis by Sales Employee" + "Items List". |
| **Odoo** | Ventas → Informes → Análisis de ventas → Exportar. |
| **ERP propio / Excel** | Lo que uses hoy, siempre que incluya las columnas de `ventas_detalle.csv`. |

> **Nota importante:** este prompt está diseñado para empresas con **equipo comercial estructurado** (vendedores asignados a zonas y familias). Si tu equipo no está así organizado, el dashboard funcionará igual pero las conclusiones tendrán menos valor. Sectores donde encaja de libro: mayorista, distribución, industria con red comercial, seguros, inmobiliaria.

---

## Columnas esperadas

**`ventas_detalle.csv`:** fecha, vendedor, zona, familia, cliente, importe, coste, unidades
**`objetivos.csv`:** vendedor, zona_principal, objetivo_mensual, objetivo_margen_pct

---

Creado por Isaac Romà · https://isaacroma.com
