# CASO 44 — EL MARGEN SE COMPRIME Y NO SABES POR QUÉ

**Pack de automatización ejecutiva para mayoristas y distribuidores PYME**
Creado por Isaac Romà · https://isaacroma.com

---

## EL PROBLEMA QUE RESUELVE

Facturas lo mismo (o más) que hace dos años, pero cada cierre te deja menos EBITDA. El margen bruto se ha comprimido 3-5 puntos y nadie en la empresa sabe decirte con precisión por qué.

Es la enfermedad silenciosa del mayorista español: la erosión viene por **cuatro frentes a la vez** y mezclarlos impide atajarla.

1. **Coste de compra** sube (proveedor repercute inflación) → generalmente inevitable, pero medible.
2. **Descuentos comerciales** crecen (comercial agresivo para no perder cliente) → evitable con política.
3. **Coste logístico** sube (transporte, última milla, almacén saturado) → corregible operativamente.
4. **Devoluciones** crecen (producto mal servido, cliente insatisfecho) → corregible con proceso.

Este pack descompone los **4,2 puntos de margen perdidos** en los últimos 24 meses y los atribuye con precisión a cada causa, con un plan de acción cuantificado para cada una.

---

## QUÉ CONTIENE EL PACK

| Archivo | Para qué sirve |
|---|---|
| `LEEME.md` | Este archivo. Léelo primero. |
| `prompt.txt` | El prompt para pegar en Claude Code. |
| `ventas_24m.csv` | 24 meses de ventas por familia, con coste de compra, descuentos, logística y devoluciones. |
| `clientes.csv` | Maestro de clientes con tipología (instalador, constructora, obra pública). |
| `proveedores.csv` | Maestro de proveedores con familia que suministran. |
| `descuentos_detalle.csv` | Detalle de descuentos aplicados por cliente y motivo. |
| `devoluciones_detalle.csv` | Detalle de devoluciones con motivo (defectuoso, mal pedido, retraso, etc.). |

Los datos son ficticios pero coherentes: representan una **Suministros Levante S.L.**, mayorista de material de fontanería, electricidad y climatización, facturación ~5M€/año, con tres familias de producto.

---

## CÓMO USARLO EN 5 MINUTOS

### Paso 1 — Instalar Claude Code (si aún no lo tienes)

```bash
npm install -g @anthropic-ai/claude-code
```

Requiere Node.js 18+. Si no sabes qué es Node, abre terminal y escribe `node --version`. Si da error, instala Node desde https://nodejs.org

### Paso 2 — Guardar los archivos del pack

Descomprime el ZIP en una carpeta accesible, por ejemplo:
```
C:\Analisis\Erosion_Margen\
```
o en Mac:
```
~/Analisis/Erosion_Margen/
```

### Paso 3 — Abrir Claude Code en esa carpeta

```bash
cd C:\Analisis\Erosion_Margen
claude
```

### Paso 4 — Pegar el prompt

Abre `prompt.txt`, cópialo entero y pégalo en Claude Code.

**Antes de pulsar Enter**, cambia estas variables:
- `[EMPRESA]` → nombre de tu empresa (ej: "Distribuciones García S.L.").
- `[MES AÑO]` → periodo que quieres analizar (ej: "septiembre 2026").
- `@ruta/` → ya está puesto como `@./` (carpeta actual), déjalo así.

Pulsa Enter. Claude Code procesará los CSVs y generará un dashboard HTML con el waterfall de erosión.

### Paso 5 — Revisar el resultado

Se abrirá automáticamente un dashboard en el navegador con:
- Waterfall de margen bruto → margen neto, por causa.
- Puntos perdidos por cada causa (coste compra, descuentos, logística, devoluciones).
- Clasificación de cada causa como **inevitable / evitable / corregible**.
- Plan de acción priorizado con impacto estimado en EBITDA.

---

## CÓMO SACAR TUS DATOS REALES DEL ERP

Esta es la pregunta del millón. Depende de tu ERP:

### A3 ERP / A3CON
Módulo *Informes de gestión* → *Ventas por familia* → exportar a Excel. Añadir columnas de coste de compra desde *Compras por artículo*. Logística suele estar en *Costes generales* → prorratear.

### Sage 50 / Sage 200
*Informes personalizados* → consulta libre sobre tablas `MovLinA` (ventas) y `MovLinC` (compras). Descuentos: campo `Descuento1` en líneas de factura. Devoluciones: documentos tipo `AB` (abonos).

### Holded
*Analytics* → *Facturación* → filtrar por categoría y descargar CSV. Coste de compra en *Inventario* → *Valoración de stock*. Logística: cuenta contable 624 (transportes).

### SAP Business One
Query Manager: `OINV` (ventas) + `INV1` (líneas) + `OPOR` (compras). Pedir al consultor que te monte una query mensual exportada.

### Odoo
Módulo *Contabilidad* → *Informes* → *Analítico* → agrupar por cuenta analítica (familia). Exportar a CSV.

### Excel/manual
Si llevas la contabilidad en Excel, el pack te sirve para entender la estructura. Monta tu CSV con las mismas columnas que `ventas_24m.csv` y funcionará igual.

---

## NOTA IMPORTANTE SOBRE SECTOR

Este prompt está **diseñado específicamente para mayoristas y distribuidores** (facturación 1-50M€, márgenes brutos 15-30%, muchos clientes B2B, múltiples familias de producto).

Si eres **fabricante** → el prompt funciona pero la causa principal será *coste de materias primas*, no *coste de compra*. Avísalo al prompt.

Si eres **retail / tienda física** → ajusta el prompt añadiendo *mermas* como quinta causa de erosión.

Si eres **servicios** → este prompt no aplica, usa el *Caso 38 — Rentabilidad por cliente de servicios*.

---

## QUÉ HACER CON EL ANÁLISIS

El dashboard te dirá en qué causa estás perdiendo más. Las acciones típicas:

- **Si pierdes por coste de compra** → renegociar con top 5 proveedores, buscar alternativas, cambiar escalados.
- **Si pierdes por descuentos** → política de descuentos escrita, cuadro de autorizaciones, formación comercial.
- **Si pierdes por logística** → auditar transportistas, revisar rutas, optimizar carga, revisar coste almacén.
- **Si pierdes por devoluciones** → análisis de causa raíz, mejorar picking, formar al equipo comercial.

Cada punto porcentual de margen recuperado en un mayorista de 5M€ son **50.000 €/año** directos al EBITDA.

---

## ¿NECESITAS AYUDA PARA APLICARLO EN TU EMPRESA?

Si quieres hacer esto con tus datos reales conectado a tu ERP, y después implementar el plan de acción con tu equipo, puedo ayudarte.

→ **Reunión gratuita de 30 min**: https://calendly.com/asesor-online-ia/30min
→ **Más casos como este**: https://isaacroma.com/blog
→ **Mi web**: https://isaacroma.com

---

*Creado por Isaac Romà · Economista · 20 años como CEO/CFO/COO de PYMEs industriales · https://isaacroma.com*
