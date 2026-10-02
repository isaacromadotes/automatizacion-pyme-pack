# 🌾 CASO 29 — Coste real por referencia para gran distribución

**Creado por Isaac Romà · https://isaacroma.com**

---

## El problema que resuelve

Mercadona, Carrefour, Lidl o Dia te piden una bajada del 3% y tú aceptas porque "aún queda margen". Pero no sabes tu **coste real**.

La mayoría de fabricantes PYME calculan el coste de sus referencias sumando solo producción. Olvidan:

- 🚚 **Logística** (transporte + manipulación hasta plataforma)
- 📉 **Merma** (producto roto, caducado, rechazado)
- 💰 **Coste financiero** del plazo de cobro (90 días de media en gran distribución)

Resultado: entre un 15% y un 25% de las referencias se venden **a pérdida real** sin que el gerente lo sepa.

Este pack te da la ficha de coste completa de cada referencia en una web interactiva. Llegas a negociar sabiendo tu número mínimo viable.

---

## Qué contiene este ZIP

```
caso_29_coste_real_mercadona/
├── LEEME.md                        ← Este archivo
├── prompt.txt                      ← El prompt para pegar en Claude Code
└── datos_ejemplo/
    ├── costes_produccion.csv       ← Coste MP + MOD + indirectos por ref
    ├── costes_logisticos.csv       ← Transporte y manipulación por ref
    ├── mermas.csv                  ← Tasa de merma por ref y canal
    ├── condiciones_cobro.csv       ← Plazos de pago y coste financiero
    └── precios_venta.csv           ← Precio de venta por ref y canal
```

---

## Cómo usarlo (5 pasos)

1. **Instala Claude Code** si no lo tienes: https://docs.claude.com/claude-code
2. **Copia esta carpeta** entera a tu equipo (ejemplo: `C:\Ejemplos\caso_29\`)
3. **Abre la terminal** en esa carpeta y escribe: `claude`
4. **Arrastra el `LEEME.md` y el `prompt.txt`** al chat de Claude Code (para que entienda el contexto completo)
5. **Pega el contenido de `prompt.txt`** y pulsa Enter

En 2 minutos tendrás una web local con la ficha de coste real de las 15 referencias.

Para usarlo con tus datos reales: sustituye los 5 CSVs por los tuyos manteniendo el mismo nombre y las mismas columnas.

---

## De dónde sacar estos datos en tu ERP

| Archivo | Dónde está en tu ERP |
|---|---|
| **costes_produccion.csv** | SAP: módulo CO-PC (Product Costing) · A3ERP: Escandallos de fabricación · Sage 200: Costes de artículos · Holded: Productos > Coste · Odoo: Fabricación > BOM + costes |
| **costes_logisticos.csv** | Suele estar fuera del ERP. Pídelo al operador logístico o calcula €/palet entre unidades por palet |
| **mermas.csv** | SAP: tabla MARD de mermas · A3/Sage: regularizaciones de almacén · O del histórico de notas de abono por calidad |
| **condiciones_cobro.csv** | Condiciones comerciales de cada cliente/canal. Coste financiero = tipo de tu póliza de crédito |
| **precios_venta.csv** | Tarifas de venta por canal, o del histórico de facturas emitidas |

👉 **Si no tienes alguno de estos datos, es la primera señal de que negocias a ciegas.** Empieza por producción + estimación de los otros tres.

---

## ⚠️ Nota importante — Sector de este caso

Este caso está diseñado para **fabricantes alimentarios que venden a gran distribución** (Mercadona, Carrefour, Lidl, Dia, Eroski, Alcampo). También aplica con pequeños cambios a:

- **Fabricantes textiles** vendiendo a El Corte Inglés, Primark, Inditex
- **Cosmética** vendiendo a Druni, Primor, cadenas de perfumerías
- **Droguería / limpieza** vendiendo a supermercados

Las fórmulas de coste financiero y merma son universales. Lo que cambia son los plazos de cobro típicos y las tasas de merma habituales.

---

## Firma

**Creado por Isaac Romà · https://isaacroma.com**
Metodología de automatización ejecutiva para PYMEs industriales españolas.
