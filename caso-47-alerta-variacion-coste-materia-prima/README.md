# Caso 47 · Alerta de variación de coste de materia prima — Detecta pérdidas antes de que lleven 90 días vendiendo bajo coste

> Cuando sube el precio de una materia prima, en minutos sabes qué referencias entran en pérdidas, cuánto margen pierdes y cuál es el PVP mínimo viable.

## 🎯 Problema que resuelve

Una PYME agroalimentaria compra aceite, harina, azúcar, carne o pescado con precios que varían cada semana, pero los PVP no se actualizan al mismo ritmo. El resultado habitual es que una subida del 14% en el aceite no se traslada al coste de producción, se sigue vendiendo al mismo precio durante tres meses y, cuando por fin se revisan los márgenes, la empresa descubre que lleva 90 días vendiendo a pérdida en varias referencias. El problema no es la subida en sí, sino el retraso entre la variación de coste y la decisión comercial: nadie tiene tiempo de recalcular manualmente escandallos, cruzarlos con la tarifa de venta vigente y marcar las referencias críticas cada vez que un proveedor manda una nueva lista de precios. Este pack automatiza ese circuito con Claude Code: detecta la variación, identifica las referencias afectadas vía escandallos, recalcula el coste de producción, compara con el PVP actual, marca las que entran en pérdidas o bajan del 15% de margen y calcula el PVP mínimo viable, entregando una alerta HTML visual y una ficha de impacto en Excel lista para llevar a dirección y a comercial.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía original del caso |
| `prompt.txt` | Prompt para pegar en Claude Code |
| `escandallos.csv` | Composición de cada producto (materia prima y cantidad) |
| `precios_mp.csv` | Precio anterior y nuevo de cada materia prima |
| `precios_venta.csv` | PVP actual de cada referencia |
| `instrucciones_diseno_excel.txt` | Diseño de la ficha Excel |
| `instrucciones_diseno_html.txt` | Diseño de la alerta HTML |

## 🚀 Cómo usarlo en 5 pasos

1. Instala Claude Code siguiendo la guía oficial en https://docs.anthropic.com/en/docs/claude-code y ejecutando `npm install -g @anthropic-ai/claude-code` (requiere Node.js; en Windows funciona con WSL o nativo).
2. Crea una carpeta en tu equipo, copia dentro todos los archivos del pack y abre la terminal en esa ruta.
3. Escribe `claude` para arrancar la sesión y arrastra `LEEME.md` y `prompt.txt` a la ventana para dar contexto.
4. Abre `prompt.txt` y sustituye las variables entre corchetes por tus datos reales: `[EMPRESA]`, `[MATERIA_PRIMA]`, `[PRECIO_ANTERIOR]`, `[PRECIO_NUEVO]`, `[MES AÑO]` y `@ruta/` apuntando a tu carpeta.
5. Pega el prompt en Claude Code y pulsa Enter. Recibirás `alerta_[EMPRESA]_[MES_AÑO].html` (para abrir en navegador) y `ficha_impacto_[EMPRESA]_[MES_AÑO].xlsx` (ficha detallada).

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Escandallos / BOM | Precios materia prima | PVP |
|---|---|---|---|
| **SAP Business One** | Producción → Lista de materiales (BOM) → Exportar CSV | Compras → Precios de artículo → Histórico | Tarifa de venta → Exportar CSV |
| **Sage 50/200** | Producción → Escandallos → Listado completo | Compras → Tarifas de proveedores | Tarifa de venta vigente → CSV |
| **A3 ERP** | Fabricación → Fichas técnicas → Exportar | Compras → Artículos → PMP | Tarifa de venta → Exportar |
| **Holded** | Inventario → Productos → Composición | Inventario → Productos → Precio coste | Tarifa venta → Exportar |
| **Odoo** | Fabricación → Lista de materiales → Exportar | Compras → Productos → Tarifa compra | Ventas → Tarifa → Exportar |

Columnas mínimas en `escandallos.csv`: `referencia`, `producto`, `materia_prima`, `cantidad_por_unidad`. Para `precios_mp.csv` exporta el precio actual y recupera el de hace 1-3 meses del histórico.

> ⚠️ **Nota de sector:** este pack está pensado para agroalimentario (conservas, platos preparados, panadería industrial, hostelería con producción propia), pero funciona en cualquier sector con escandallos o BOM: metalmecánica, construcción, textil, química o cosmética. Solo adapta los nombres de materias primas y productos. Si tu problema es más amplio que una materia prima concreta, mira también [caso-44 (erosión de margen mayorista)](../caso-44-erosion-margen-mayorista/) y [caso-37 (coste real PYME industrial)](../caso-37-coste-real-pyme-industrial/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años de C-Suite. Trabajo con PYMEs de 1-50M€ en industria, mayoristas y construcción.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 Reserva 30 min: https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>alerta variación coste materia prima pyme, recalcular escandallos automático, control margen agroalimentario, automatización coste producción claude code, pvp mínimo viable escandallo, impacto subida aceite margen, ficha impacto materia prima excel, alerta pérdidas por referencia, consultor automatización IA pyme agroalimentaria, escandallos sap sage holded odoo</sub>
