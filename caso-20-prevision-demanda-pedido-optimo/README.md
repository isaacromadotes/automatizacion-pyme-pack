# Caso 20 · Previsión de demanda y pedido óptimo — Mayorista sin sobrestock ni roturas

> **89.000 €** parados en sobrestock, **8 referencias en rotura semanal** (3 de clase A). Pasa de pedir "lo de siempre" a un sistema de reaprovisionamiento profesional en **2-3 minutos**.

## 🎯 Problema que resuelve

En un mayorista o distribuidor con catálogo de 500 a 5.000 referencias, el responsable de compras lleva veinte años pidiendo "lo de siempre" a cada proveedor. Su intuición era buena cuando el mercado era estable, pero hoy el patrón de demanda cambia cada trimestre, los plazos de proveedor se alargan sin avisar y la empresa acumula dos problemas opuestos que conviven en el mismo almacén: capital parado en sobrestock de referencias que ya no rotan y rotura de stock en referencias clase A que son precisamente las que más facturan. En una PYME tipo son fácilmente 89.000 € inmovilizados en producto con más de 180 días de cobertura mientras se pierden ventas semanales por falta de disponibilidad. Las decisiones de compra se hacen a ojo porque nadie tiene tiempo de cruzar el histórico real de ventas con el plazo de entrega del proveedor, el stock actual y los pedidos que ya están en camino pero aún no han llegado. Este pack ejecuta un sistema de reaprovisionamiento completo en una sola pasada: previsión de demanda a 4 semanas por referencia, cálculo de punto de reorden y stock de seguridad en función del plazo de proveedor, detección automática de sobrestock y rotura, y propuesta de pedido óptimo agrupado por proveedor para minimizar portes y aprovechar escalados. El comprador deja de adivinar y pasa a revisar y validar.

## 📦 Archivos del pack

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Documento inicial con la explicación del caso. |
| `prompt.txt` | Prompt listo para pegar en Claude Code. |
| `ventas_12m.csv` | Histórico de ventas semanales de los últimos 12 meses (60 referencias × 52 semanas). |
| `stock_actual.csv` | Stock actual por referencia, coste unitario, proveedor y plazo de entrega. |
| `pedidos_pendientes.csv` | Pedidos cursados aún no recepcionados, con cantidad y fecha prevista. |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la [documentación oficial](https://docs.anthropic.com/en/docs/claude-code): `npm install -g @anthropic-ai/claude-code`
2. **Descomprime este pack** en una carpeta local (ej. `C:\Reaprovisionamiento\`) y abre la terminal dentro con el comando `claude`.
3. **Arrastra a la ventana de Claude Code** el `LEEME.md`, el `prompt.txt` y los 3 CSV para que tenga todo el contexto.
4. **Copia el contenido de `prompt.txt`**, pégalo en Claude Code y sustituye las variables entre corchetes (empresa, mes, ruta) por tus datos reales.
5. **Pulsa Enter**: en 2-3 minutos Claude Code genera el dashboard HTML con alertas visuales, el Excel con todas las referencias analizadas y el pedido óptimo agrupado por proveedor listo para revisar.

## 🔌 Cómo exportar los datos desde tu ERP

| Dato | A3ERP / A3 Innuva | Sage 50/200 | Holded | SAP Business One | Odoo |
|---|---|---|---|---|---|
| Ventas 12 meses por artículo/semana | Ventas → Estadísticas → Ventas por artículo y periodo | Ventas → Consultas → Ventas por artículo → Exportar | Ventas → Facturas → Filtro 12 meses → Exportar líneas | Ventas → Informe de ventas por artículo (agrupar semana) | Ventas → Informes → Análisis por producto/semana |
| Stock actual + coste + proveedor + plazo | Almacén → Stock por referencia + ficha proveedor | Almacén → Stock + ficha artículo (plazo) | Inventario → Stock + ficha producto | Inventario → Stock + ficha maestra artículo | Inventario → Stock → Exportar con proveedor y lead time |
| Pedidos de compra pendientes | Compras → Pedidos abiertos → Exportar | Compras → Pedidos pendientes de recepción | Compras → Pedidos → Filtro "pendiente" | Compras → Pedidos de compra abiertos | Compras → Pedidos → Estado "en recepción" |

> ⚠️ **Nota de sector:** este pack está pensado para **mayoristas y distribuidores** con catálogo de 500-5.000 referencias, plazos de proveedor conocidos y demanda con cierta recurrencia (material industrial, ferretería, suministros, e-commerce con almacén propio, fabricantes que reponen componentes). Si trabajas con producto perecedero (frescos, farma), proyecto único o gran cuenta con contrato marco, el stock de seguridad y la ventana de previsión necesitan ajustes. Para completar el circuito de almacén y compras, combina con el [caso-07 (diagnóstico de inventario)](../caso-07-diagnostico-inventario/) y el [caso-11 (pedidos EDI)](../caso-11-pedidos-edi/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años en C-Suite.
Ayudo a **PYMEs industriales, mayoristas y de construcción (1-50M€)** a automatizar operaciones y recuperar margen con IA aplicada al negocio real, no a la tecnología.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **Automatización a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min conmigo:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>previsión demanda mayorista automática, punto de reorden stock seguridad, pedido óptimo agrupado proveedor, reaprovisionamiento automatizado pyme, detectar sobrestock y rotura, forecast ventas 4 semanas distribución, lead time proveedor cálculo stock, dashboard compras mayorista, reducir inmovilizado almacén, sistema reposición distribuidor industrial</sub>
