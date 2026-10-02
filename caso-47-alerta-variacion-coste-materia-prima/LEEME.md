# Caso 47 — Alerta de variación de coste de materia prima

## El problema que resuelve

Eres una PYME agroalimentaria. Compras aceite, harina, azúcar, carne, pescado… y los precios de tus materias primas **cambian cada semana**.

Pero tus PVP no cambian al mismo ritmo. Resultado:

- Sube el aceite un 14% y no actualizas el coste de producción.
- Sigues vendiendo al mismo precio durante 3 meses.
- Cuando revisas márgenes, descubres que **llevas 90 días vendiendo a pérdida** en varias referencias.

Este pack usa Claude Code para:

1. Detectar la variación de precio en una materia prima.
2. Identificar todas las referencias afectadas (vía escandallos).
3. Recalcular el coste de producción de cada una.
4. Comparar con el PVP actual.
5. Marcar las que entran en pérdidas o bajan del 15% de margen.
6. Calcular el PVP mínimo viable para cada una.
7. Generar una **alerta HTML visual** + una **ficha impacto Excel**.

Todo en minutos, sin tocar hojas de cálculo manualmente.

---

## Qué contiene este ZIP

- `LEEME.md` → este archivo
- `prompt.txt` → el prompt para pegar en Claude Code
- `escandallos.csv` → composición de cada producto (qué materia prima y cuánta lleva)
- `precios_mp.csv` → precio anterior y nuevo de cada materia prima
- `precios_venta.csv` → PVP actual de cada referencia
- `instrucciones_diseno_excel.txt` → cómo debe diseñarse la ficha Excel
- `instrucciones_diseno_html.txt` → cómo debe diseñarse la alerta HTML

---

## Cómo usarlo paso a paso

1. **Instala Claude Code** (si aún no lo tienes):
   - Guía oficial: https://docs.claude.com/claude-code
   - Requiere Node.js. En Windows funciona con WSL o nativo.

2. **Crea una carpeta en tu equipo** y copia dentro todos los archivos de este ZIP.
   Ejemplo de ruta en Windows:
   `C:\Users\TuUsuario\Descargas\caso_47_alerta_mp\`

3. **Abre tu terminal** en esa carpeta y escribe:
   ```
   claude
   ```

4. **Arrastra a Claude Code** los archivos `LEEME.md` y `prompt.txt` para que la IA tenga el contexto completo antes de ejecutar.

5. **Abre `prompt.txt`**, cambia las variables entre corchetes por tus datos reales:
   - `[EMPRESA]` → el nombre de tu empresa
   - `[MATERIA_PRIMA]` → la materia prima que ha variado (ej: "Aceite de oliva virgen extra")
   - `[PRECIO_ANTERIOR]` → precio por litro/kg anterior
   - `[PRECIO_NUEVO]` → precio por litro/kg nuevo
   - `[MES AÑO]` → mes y año del análisis
   - `@ruta/` → ruta a tu carpeta con los CSVs

6. **Pega el prompt completo en Claude Code** y pulsa Enter.

7. **Recibirás 2 archivos** en la misma carpeta:
   - `alerta_[EMPRESA]_[MES_AÑO].html` → alerta visual para abrir en navegador
   - `ficha_impacto_[EMPRESA]_[MES_AÑO].xlsx` → ficha Excel detallada

---

## De dónde sacar los datos en tu ERP

### `escandallos.csv` — Composición de productos

| ERP | Dónde encontrarlo |
|-----|-------------------|
| **SAP Business One** | Producción → Lista de materiales (BOM) → Exportar a CSV |
| **Sage 50/200** | Producción → Escandallos → Listado completo |
| **A3 ERP** | Fabricación → Fichas técnicas → Exportar |
| **Odoo** | Fabricación → Lista de materiales → Exportar |
| **Holded** | Inventario → Productos → Composición (en productos de fabricación) |

Columnas mínimas: `referencia`, `producto`, `materia_prima`, `cantidad_por_unidad`

### `precios_mp.csv` — Precios de materias primas

| ERP | Dónde encontrarlo |
|-----|-------------------|
| **SAP B1** | Compras → Precios de artículo → Histórico |
| **Sage** | Compras → Tarifas de proveedores |
| **A3 ERP** | Compras → Artículos → Precio medio ponderado |
| **Odoo** | Compras → Productos → Tarifa de compra |
| **Holded** | Inventario → Productos → Precio de coste |

Exporta precio actual (precio_nuevo) y recupera el precio de hace 1-3 meses del histórico.

### `precios_venta.csv` — PVP actuales

| ERP | Dónde encontrarlo |
|-----|-------------------|
| Cualquier ERP | Tarifa de venta vigente → Exportar a CSV |

---

## Nota importante

Este prompt está diseñado para el **sector agroalimentario** (conservas, platos preparados, panadería industrial, hostelería con producción propia), pero funciona igual en cualquier sector con escandallos o lista de materiales:

- Industria metalmecánica (acero, aluminio, cobre)
- Construcción (cemento, hierro, madera)
- Textil (algodón, poliéster)
- Química (reactivos, disolventes)
- Cosmética (aceites esenciales, principios activos)

Solo tienes que adaptar los nombres de las materias primas y los productos.

---

*Creado por Isaac Romà · https://isaacroma.com*
