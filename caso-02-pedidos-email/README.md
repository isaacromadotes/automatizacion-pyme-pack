# Caso 02 · Pedidos por Email al ERP — De 3 minutos a 15 segundos sin errores

> Pack listo para implementar en mayoristas y distribución. Resultado: pedidos del email introducidos en el ERP automáticamente, con validación de catálogo y stock. Ahorro medio: 105 min/día (35 pedidos × 3 min).

## 🎯 Problema que resuelve

En empresas mayoristas y de distribución, alguien del equipo copia pedidos del email (o WhatsApp) al ERP a mano. Línea por línea. Con 35 pedidos/día y 3 min cada uno, son **105 minutos diarios** copiando datos — y cada error de referencia, cantidad o precio llega al cliente. Este pack lee el email, identifica al cliente, valida referencias contra tu catálogo y comprueba stock. Si algo no cuadra, lo marca como excepción.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía original del caso |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `email_pedido.txt` | Email ficticio de un cliente (10 referencias) |
| `catalogo_productos.csv` | Catálogo con 20 referencias, precios y familias |
| `stock_actual.csv` | Stock disponible y mínimos por referencia |
| `clientes.csv` | Base de 5 clientes con descuentos y condiciones |

## 🚀 Cómo usarlo en 5 pasos

1. **Descarga** los archivos de esta carpeta.
2. **Abre** `prompt.txt` y cópialo.
3. **Pégalo** en Claude Code ([instalación aquí](https://docs.anthropic.com/en/docs/claude-code)).
4. **Cambia** `[EMPRESA]` y `@ruta/` por tus datos reales.
5. **Pulsa Enter**: Claude Code generará el pedido completo (precios, descuentos, IVA, totales) en una web lista para revisar.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Catálogo | Stock | Clientes |
|---|---|---|---|
| **A3 / Wolters Kluwer** | Almacén → Artículos → Exportar | Almacén → Stocks → Exportar | Ventas → Clientes → Exportar |
| **Sage 50 / 200** | Inventario → Artículos → Excel | Inventario → Existencias | Ventas → Clientes |
| **Holded** | Productos → Exportar CSV | Productos → Stock | Contactos → Clientes → Exportar |
| **SAP Business One** | MM60 / tabla MARA | MMBE o MB52 | XD03 / tabla KNA1 |
| **Odoo** | Inventario → Productos → Exportar | Inventario → Informes → Existencias | Contactos → Exportar |

⚠️ **Diseñado para mayoristas y distribución** (suministros industriales, ferretería, material eléctrico, fontanería). Para alimentación, textil o farmacia hay que ajustar familias y columnas del catálogo.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con 20 años en C-Suite. Ayudo a PYMEs españolas (1-50M€) de industria, mayoristas y construcción a automatizar su gestión con IA.

**Servicios:**
- 🔍 **Diagnóstico de automatización**: 750€
- ⚙️ **Automatización llave en mano**: desde 4.500€
- 🤝 **Acompañamiento mensual**: 300€/mes

👉 **Reserva 30 min gratis**: [calendly.com/asesor-online-ia/30min](https://calendly.com/asesor-online-ia/30min)

---

**Isaac Romà** · Consultor de automatización IA para PYMEs
🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://linkedin.com/in/isaacroma) · 💻 [GitHub](https://github.com/isaacromadotes)

---

<sub>**Keywords**: pedidos email automatizados, OCR pedidos mayorista, automatización ERP distribución, Claude Code pedidos, entrada pedidos sin errores, integración email ERP, mayorista automatización IA, picking automatizado, validación referencias catálogo, consultor automatización mayorista España.</sub>
