# CASO 37 — Precio fijado "como siempre" sin saber el coste real

## El problema

Llevas años aplicando la misma lista de precios con pequeñas subidas lineales. Pero el acero ha subido, la mano de obra ha subido, la luz y el gas se han disparado y los indirectos nadie los reparte bien entre referencias.

Resultado: **tienes productos que vendes a pérdida sin saberlo**. Y los descuentos que das a tus mejores clientes, directamente, los pagas tú.

Este caso resuelve esto en minutos: cruza escandallos + precios de compra actualizados + tiempos reales de producción + indirectos, y te da el coste unitario real, el margen por referencia y el precio mínimo viable al 20%.

---

## Qué contiene este ZIP

- **LEEME.md** — este archivo
- **prompt.txt** — el prompt que pegarás en Claude Code
- **escandallos.csv** — materiales y cantidades por referencia (BOM)
- **precios_compra.csv** — precios actualizados de materias primas por proveedor
- **tiempos_produccion.csv** — minutos de mano de obra por referencia y operario
- **indirectos.csv** — costes indirectos mensuales de la planta
- **precios_venta.csv** — PVP actual por referencia y cliente principal

---

## Cómo usarlo paso a paso

1. **Instala Claude Code** si aún no lo tienes: https://claude.com/claude-code
2. **Copia esta carpeta** completa a una ruta accesible (ej. `C:\Users\TU_USUARIO\Descargas\caso_37\` o `~/Descargas/caso_37/`)
3. **Abre tu terminal** (iTerm, CMD, PowerShell o Terminal) y escribe `claude`
4. **Arrastra el LEEME.md y el prompt.txt a la ventana de Claude Code** junto con los CSVs — así la IA entiende el contexto completo antes de ejecutar
5. **Abre el prompt.txt**, cambia las variables (`[EMPRESA]`, `[MES AÑO]`, rutas) por los tuyos
6. **Pega el prompt** en Claude Code y pulsa Enter
7. Claude Code generará: tabla web interactiva + Excel de escandallo + alertas PDF

---

## De dónde sacar los datos en tu ERP

| CSV | Dónde está en tu ERP |
|---|---|
| `escandallos.csv` | **A3 ERP**: Fabricación → Escandallos / BOM. **Sage 200**: Producción → Estructuras. **Holded**: Productos → Escandallo. **SAP**: CS03 (lista de materiales). **Odoo**: Fabricación → Listas de materiales |
| `precios_compra.csv` | **A3**: Compras → Tarifas proveedor. **Sage**: Proveedores → Tarifas. **Holded**: Contactos → Proveedores → Tarifas. **SAP**: ME1L. **Odoo**: Compras → Proveedores → Lista de precios |
| `tiempos_produccion.csv` | **A3**: Fabricación → Rutas de producción. **Sage**: Producción → Fases. **SAP**: CA03 (hoja de ruta). **Odoo**: Fabricación → Operaciones. Si no lo tienes digitalizado, exporta el último parte de producción del mes |
| `indirectos.csv` | Tu **contabilidad analítica** del último mes cerrado. **Sage**: Analítica → Centros de coste. **A3**: Contabilidad analítica. Alternativa: la suma de gastos del grupo 62 del PGC del mes |
| `precios_venta.csv` | **A3/Sage/Holded**: Ventas → Tarifas de venta. **SAP**: VK13. **Odoo**: Ventas → Productos → Lista de precios |

---

## Nota importante

Este prompt está diseñado para **PYMEs industriales / metalúrgicas / fabricación en serie**.

Si tu negocio es:
- **Mecanizado por encargo** → funciona igual, pero sustituye "unidades producidas" por "horas facturables"
- **Hostelería** → usa el caso de escandallo de plato en vez de este
- **Distribución pura (sin fabricación)** → usa el caso de margen por referencia (sin tiempos de MO)

---

## Firma

Creado por Isaac Romà · https://isaacroma.com
Economista con 20 años como CEO/CFO/COO en PYMEs industriales españolas.
