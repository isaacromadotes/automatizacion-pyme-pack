# Caso 50 · Stock sin rotación — 72.400 € inmovilizados invisibles, 45.000 € recuperables

> Cruza stock actual y movimientos de 12 meses, detecta qué referencias llevan más de 180 días paradas, cuánto cuestan al año y qué hacer con cada una.

## 🎯 Problema que resuelve

Entre un 10% y un 20% del stock de cualquier mayorista o distribuidor lleva meses sin moverse, pero no aparece como problema porque "en el ERP sale que tengo stock". Ese capital inmovilizado paga coste financiero vía póliza o préstamo, ocupa espacio de almacén que podría destinarse a referencias con rotación y acumula riesgo de obsolescencia, mermas o devaluación. El dato invisible — cuánto dinero concreto hay parado, cuánto cuesta al año, qué referencias conviene devolver al proveedor, liquidar o promocionar — nadie lo construye porque exige cruzar manualmente la valoración de inventario con los movimientos de los últimos 12 meses, aplicar un umbral de días sin rotación, imputar coste financiero y de almacenamiento, y priorizar acciones referencia a referencia. Este pack usa Claude Code para automatizar todo el circuito: identifica las referencias con más de 180 días sin movimiento, calcula capital inmovilizado y coste anual oculto (interés de la póliza + coste de m² de almacén), estima la recuperación realista por tipo de acción y entrega un informe HTML visual más un Excel ejecutivo con el plan de acción listo para llevar al lunes. Datos del ejemplo (mayorista de fontanería): 34 referencias, 72.400 € inmovilizados, 8.200 €/año de coste invisible y 45.000 € recuperables.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía original del caso |
| `prompt.txt` | Prompt para pegar en Claude Code |
| `stock_actual.csv` | Inventario de ejemplo (74 referencias mayorista fontanería) |
| `movimientos_12m.csv` | Movimientos del último año (1.279 entradas/salidas) |
| `diseno_html.txt` | Instrucciones de diseño del informe HTML |
| `diseno_excel.txt` | Instrucciones de diseño del Excel resumen |

## 🚀 Cómo usarlo en 5 pasos

1. Instala Claude Code siguiendo la guía oficial en https://docs.anthropic.com/en/docs/claude-code y ejecutando `npm install -g @anthropic-ai/claude-code` (requiere Node.js).
2. Descomprime el ZIP en una carpeta (ej. `C:\Descargas\caso_50_stock_muerto\`) y abre la terminal allí.
3. Escribe `claude` y arrastra `LEEME.md` y `prompt.txt` a la conversación para dar contexto.
4. En `prompt.txt`, sustituye `[EMPRESA]`, `[MES AÑO]`, `[TASA_INTERES]` (tipo de tu póliza, ej. 7,5) y `[COSTE_ALMACEN_M2]` (déjalo en 15 € si no lo sabes).
5. Pega el prompt y pulsa Enter. En ~2 minutos tendrás el informe HTML abierto en el navegador y el Excel `informe_stock_muerto.xlsx` con tres hojas (Resumen, Detalle, Plan de Acción).

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Stock actual valorado | Movimientos 12 meses |
|---|---|---|
| **SAP Business One** | Inventario → Informes → Lista de artículos valorada | Inventario → Historial de artículos → Rango 365 días |
| **Sage 50/200** | Stocks → Informes → Existencias valoradas → CSV | Stocks → Movimientos → Rango 12 meses → Exportar |
| **A3 ERP / A3 Innuva** | Almacén → Listados → Stock valorado → Excel | Almacén → Movimientos → Últimos 365 días |
| **Holded** | Inventario → Productos → Exportar (añadir "Última venta") | Inventario → Movimientos → Exportar |
| **Odoo** | Inventario → Informes → Valoración de inventario → CSV | Inventario → Transferencias → Filtrar fechas → CSV |

Columnas mínimas en `stock_actual.csv`: `ref`, `descripcion`, `stock`, `coste_unitario`, `ultimo_movimiento`. En `movimientos_12m.csv`: `ref`, `fecha`, `tipo`, `cantidad`. Si tu ERP exporta con otros nombres de cabecera, díselo a Claude Code en el prompt y lo adapta.

> ⚠️ **Nota de sector:** pensado para mayoristas, distribuidores y empresas con almacén propio (fontanería, ferretería, suministros industriales, alimentación, textil, componentes). Funciona en cualquier sector con stock físico y rotación medible; no aplica a servicios ni empresas sin stock. Para fabricantes bajo pedido, 180 días puede ser un umbral corto: ajústalo en el prompt. Si quieres completar la mirada operativa del almacén, encadénalo con [caso-44 (erosión de margen mayorista)](../caso-44-erosion-margen-mayorista/) y [caso-32 (forecast tesorería mayorista)](../caso-32-forecast-tesoreria-mayorista/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años de C-Suite. Trabajo con PYMEs de 1-50M€ en industria, mayoristas y construcción.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 Reserva 30 min: https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>stock muerto mayorista pyme, referencias sin rotación 180 días, capital inmovilizado almacén, coste financiero stock parado, análisis rotación inventario claude code, plan liquidación stock obsoleto, informe stock muerto excel html, consultor automatización almacén pyme, detección stock sin movimiento erp, recuperar caja stock inmovilizado</sub>
