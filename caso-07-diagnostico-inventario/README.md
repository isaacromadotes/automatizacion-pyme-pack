# Caso 07 · Diagnóstico de inventario — Libera capital inmovilizado y evita roturas de stock

> **Resultado clave:** Clasifica ABC tus referencias, cuantifica el sobrestock en euros y detecta roturas antes de que paren producción. En una PYME industrial típica con 400.000€ en almacén, libera entre 60.000€ y 120.000€ de caja inmovilizada en el primer análisis.

## 🎯 Problema que resuelve

En la mayoría de PYMEs industriales y de fabricación el inventario es la mayor partida de capital circulante y, al mismo tiempo, la peor gestionada. El responsable de compras pide "por intuición" o por histórico, el almacén se llena de referencias que no rotan y aun así producción se para cada mes porque falta una pieza crítica con lead time largo. El resultado: cientos de miles de euros inmovilizados en stock muerto mientras la fábrica sufre roturas evitables, caja comprometida sin control y nadie sabe exactamente qué sobra ni qué falta. Este caso automatiza el diagnóstico completo del inventario: clasificación ABC por consumo y valor, cálculo de cobertura real por referencia, detección de sobrestock cuantificado en euros, alertas de rotura inminente cruzando stock actual con órdenes de producción pendientes y lead time de proveedor, y recomendaciones concretas de compra y liquidación. Pensado para PYMEs industriales de 1-50M€ donde el inventario representa entre el 15% y el 30% del balance.

## 📦 Archivos del pack

| Archivo | Descripción |
|---------|-------------|
| `LEEME.md` | Instrucciones de uso del caso |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `maestro_articulos.csv` | Maestro de 150 referencias con stock, costes y lead times |
| `consumos_12m.csv` | Consumos mensuales de los últimos 12 meses (1.800 registros) |
| `ordenes_produccion.csv` | Órdenes de producción pendientes (8 órdenes, 91 líneas) |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** si aún no lo tienes: `npm install -g @anthropic-ai/claude-code` (requiere Node.js 18+ y cuenta Anthropic con API key). Guía oficial: [docs.anthropic.com/en/docs/claude-code](https://docs.anthropic.com/en/docs/claude-code)
2. **Copia los 3 CSVs** del pack a una carpeta de tu ordenador (ej: `C:\Users\TU_USUARIO\Downloads\Inventario\`).
3. **Abre tu terminal** (CMD, PowerShell o Terminal en Mac) y lanza `claude` desde la carpeta donde están los archivos.
4. **Pega el `prompt.txt`** y antes de pulsar Enter sustituye las variables: `[EMPRESA]` por el nombre de tu empresa, `[MES AÑO]` por el período a analizar (ej. "Septiembre 2026") y `@ruta/` por la ruta real de tus CSVs.
5. **Pulsa Enter y espera** (~2-3 min). Claude Code cruza los tres archivos, clasifica ABC, detecta sobrestock y roturas, y genera un dashboard HTML interactivo + Excel con 4 pestañas + PDF ejecutivo.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Maestro artículos | Consumos 12 meses | Órdenes de producción |
|-----|-------------------|-------------------|------------------------|
| **A3 (A3 ERP / A3 Innuva)** | Almacén → Artículos → Exportar | Almacén → Movimientos → Filtrar salidas | Producción → Órdenes activas |
| **Sage 200** | Inventario → Artículos | Movimientos de almacén → Salidas | Fabricación → Órdenes |
| **Holded** | Inventario → Productos | Inventario → Movimientos | Fabricación → Órdenes |
| **SAP Business One** | Transacción MM01 / MM60 | MB52 + MC.9 (consumo histórico) | CO03 → Lista de órdenes |
| **Odoo** | Inventario → Productos → Exportar | Inventario → Informes → Movimientos | Fabricación → Órdenes de producción |

⚠️ **Nota de sector:** Este caso está optimizado para **empresas industriales y de fabricación** (metalurgia, plásticos, alimentación, packaging, químico). Si tu empresa es de **distribución, mayorista o comercio**, ajusta los umbrales de cobertura en el prompt: el sobrestock en distribución se mide en semanas, no en meses, y la rotación mínima aceptable es mucho mayor. Para construcción, el análisis de inventario se sustituye por el **Caso 03 · Control de obra**.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con 20 años en C-Suite. Ayudo a PYMEs españolas de **1-50M€** (industria, mayoristas y construcción) a automatizar procesos ejecutivos y traducir operaciones a impacto financiero real (EBITDA, caja, margen).

- **Diagnóstico inicial:** 750€
- **Automatización a medida:** desde 4.500€
- **Acompañamiento mensual:** 300€/mes

👉 **Reserva 30 min gratis:** [calendly.com/asesor-online-ia/30min](https://calendly.com/asesor-online-ia/30min)

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>diagnóstico inventario PYME, análisis ABC stock, sobrestock capital inmovilizado, rotura de stock industrial, automatización inventario Claude Code, consultor IA PYME España, gestión almacén PYME, cobertura stock lead time, dashboard inventario industrial, optimización circulante PYME</sub>
