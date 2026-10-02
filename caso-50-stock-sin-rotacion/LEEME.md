# 📦 Caso 50 — Stock sin rotación: 72.000€ parados invisibles

## El problema real

Eres mayorista, distribuidor o tienes almacén. Compras producto, lo pones en estantería y lo vendes. Hasta aquí todo normal.

**El problema invisible**: entre 10% y 20% de tu stock lleva meses sin moverse. Capital inmovilizado. Coste financiero del préstamo que lo pagó. Espacio ocupado. Riesgo de obsolescencia.

Y nadie lo mira porque "en el ERP sale que tengo stock".

Este prompt coge dos ficheros que ya tienes (stock actual + movimientos de los últimos 12 meses), cruza las referencias y te dice:

- Qué referencias llevan más de 180 días sin movimiento
- Cuánto dinero tienes parado en ellas
- Cuánto te cuesta esa inversión bloqueada al año (coste financiero + almacenamiento)
- Qué hacer con cada una: devolver al proveedor, liquidar, promocionar

Datos del ejemplo: **34 referencias · 72.400€ inmovilizados · 8.200€/año de coste invisible · 45.000€ recuperables**.

---

## Qué contiene este ZIP

- `LEEME.md` → este archivo
- `prompt.txt` → el prompt que pegas en Claude Code
- `stock_actual.csv` → inventario de ejemplo (74 referencias de un mayorista de fontanería)
- `movimientos_12m.csv` → movimientos del último año (1.279 entradas/salidas)
- `diseno_html.txt` → instrucciones para que Claude Code genere el informe HTML con estilo
- `diseno_excel.txt` → instrucciones para que Claude Code genere el Excel resumen

---

## Cómo usarlo paso a paso

1. **Instala Claude Code** (si no lo tienes):
   - Ve a https://claude.com/claude-code
   - Instala Node.js (si no lo tienes) y luego ejecuta `npm install -g @anthropic-ai/claude-code`
   - Abre tu terminal (CMD, PowerShell, iTerm, Terminal...) y escribe: `claude`

2. **Descomprime este ZIP** en una carpeta de tu ordenador. Ejemplo: `C:\Descargas\caso_50_stock_muerto\`

3. **Abre Claude Code** en esa carpeta:
   - En Windows: abre CMD, escribe `cd C:\Descargas\caso_50_stock_muerto` y luego `claude`
   - En Mac: abre Terminal, escribe `cd ~/Descargas/caso_50_stock_muerto` y luego `claude`

4. **Abre `prompt.txt`**, cópialo entero y pégalo en Claude Code.

5. **Cambia las variables** antes de pulsar Enter:
   - `[EMPRESA]` → nombre de tu empresa
   - `[MES AÑO]` → mes y año de análisis (ej: "Septiembre 2026")
   - `[TASA_INTERES]` → el tipo de tu póliza de crédito o préstamo (ej: 7,5)
   - `[COSTE_ALMACEN_M2]` → coste mensual de almacén por m² (déjalo en 15€ si no lo sabes)

6. **Pulsa Enter**. Claude Code analiza, genera el HTML y el Excel y abre el informe en tu navegador.

---

## De dónde sacar los datos reales en tu ERP

Para usar esto con TU empresa, necesitas 2 exportaciones:

### `stock_actual.csv` — Columnas: `ref, descripcion, stock, coste_unitario, ultimo_movimiento`

- **A3 ERP / A3 Innuva**: Almacén → Listados → Stock valorado → Exportar a Excel
- **Sage 50 / Sage 200**: Stocks → Informes → Existencias valoradas → Exportar CSV
- **Holded**: Inventario → Productos → Exportar (añade columna "Última venta")
- **Odoo**: Inventario → Informes → Valoración de inventario → Exportar
- **SAP Business One**: Inventario → Informes de inventario → Lista de artículos → Exportar

### `movimientos_12m.csv` — Columnas: `ref, fecha, tipo, cantidad`

- **A3 ERP**: Almacén → Movimientos → Filtrar últimos 365 días → Exportar
- **Sage**: Stocks → Movimientos → Rango de fechas 12 meses → Exportar
- **Holded**: Inventario → Movimientos → Exportar
- **Odoo**: Inventario → Operaciones → Transferencias → Filtrar fechas → Exportar
- **SAP B1**: Inventario → Informes → Historial de artículos → Exportar

Si tu ERP exporta columnas con otros nombres, no pasa nada: dile a Claude Code en el prompt "las columnas se llaman X, Y, Z" y lo adaptará solo.

---

## ⚠️ Nota importante sobre el sector

Este ejemplo está pensado para **mayoristas, distribuidores y empresas con almacén propio** (fontanería, ferretería, suministros industriales, alimentación, textil, componentes...).

- Funciona igual de bien para cualquier sector con stock físico y rotación medible.
- Para **servicios** o **empresas sin stock**, este prompt no aplica.
- Para **fabricantes**, los umbrales de "stock muerto" pueden ser distintos (180 días es corto si fabricas bajo pedido): ajusta el parámetro en el prompt.

---

## Qué vas a obtener

Después de pulsar Enter, en ~2 minutos tendrás:

1. **Informe HTML visual** → se abre solo en tu navegador. Verás:
   - Resumen ejecutivo (capital parado, coste anual, recuperación estimada)
   - Tabla de las 34 refs con días sin movimiento, valor y acción recomendada
   - Gráfico de distribución del stock muerto por categoría de acción
   - Lista priorizada de qué hacer esta semana

2. **Excel resumen** → `informe_stock_muerto.xlsx` con tres hojas:
   - "Resumen" → KPIs y totales
   - "Stock Muerto Detalle" → una fila por referencia con toda la info
   - "Plan de Acción" → agrupado por tipo de acción (devolver, liquidar, promocionar)

Imprimes el Excel, lo llevas a tu reunión del lunes y tienes el plan de acción listo.

---

Creado por Isaac Romà · https://isaacroma.com
