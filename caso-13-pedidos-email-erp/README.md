# Caso 13 · Del email al ERP sin teclear — Procesa pedidos B2B en segundos y con cero errores

> **Resultado clave:** Lee pedidos entrantes por email, identifica cliente, cruza referencias con catálogo, valida stock y precio, aplica descuento pactado y genera pedido + albarán + confirmación. Elimina 5h/día de tecleo manual y los 8-10 errores de transcripción al mes que generan devoluciones.

## 🎯 Problema que resuelve

Todos los días, en cualquier PYME industrial o mayorista B2B, alguien del equipo administrativo abre emails de pedido, los lee uno a uno y los teclea manualmente en el ERP. El flujo típico ocupa 15 minutos por pedido: identificar al cliente a partir del remitente, buscar cada referencia en el catálogo (muchas veces el cliente usa su propia nomenclatura), comprobar stock disponible, mirar el precio tarifa, aplicar el descuento pactado, generar el pedido, lanzar el albarán y reenviar confirmación. A 20 pedidos diarios son **5 horas de una persona** dedicadas íntegramente a transcribir texto libre a campos estructurados — un trabajo sin valor añadido que además genera entre 8 y 10 errores de tecleo al mes: referencias confundidas, cantidades alteradas, descuentos mal aplicados, albaranes incorrectos, devoluciones, reclamaciones y facturas que hay que rehacer. Este caso automatiza el proceso completo: lectura e interpretación del email de pedido (texto libre, formato libre, con o sin adjunto), identificación automática del cliente por CIF o email, cruce de referencias con el catálogo maestro, validación de stock disponible y precio tarifa, aplicación del descuento y condiciones de pago del cliente, detección de incidencias (producto no en catálogo, rotura de stock, importe fuera de rango habitual) y generación del pedido estructurado + albarán + email de confirmación. Pensado para PYMEs industriales y mayoristas B2B de 1-50M€ que reciben pedidos por email de clientes recurrentes.

## 📦 Archivos del pack

| Archivo | Descripción |
|---------|-------------|
| `LEEME.md` | Instrucciones de uso del caso |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `pedidos_email.csv` | 4 emails de pedido de ejemplo (clientes industriales) |
| `clientes.csv` | Ficha de clientes con CIF, condiciones de pago y descuento |
| `productos.csv` | Catálogo con precio unitario e IVA |
| `stock.csv` | Existencias actuales, stock mínimo y ubicación en almacén |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** si aún no lo tienes: `npm install -g @anthropic-ai/claude-code` (requiere Node.js 18+ y cuenta Anthropic con API key). Guía oficial: [docs.anthropic.com/en/docs/claude-code](https://docs.anthropic.com/en/docs/claude-code)
2. **Copia los 4 CSVs** del pack a una carpeta de tu ordenador (ej: `C:\Users\TU_USUARIO\Downloads\Pedidos ERP\`).
3. **Abre tu terminal** (CMD, PowerShell o Terminal en Mac) y lanza `claude` desde la carpeta donde están los archivos.
4. **Pega el `prompt.txt`** y antes de pulsar Enter sustituye las variables: `[EMPRESA]` por el nombre de tu empresa, `[MES AÑO]` por el período a analizar y `@ruta/` por la ruta real de tus CSVs.
5. **Pulsa Enter y espera**. Claude Code lee los emails, cruza clientes y referencias, valida stock y precio, aplica descuentos y arranca una web local con los pedidos estructurados, albaranes y emails de confirmación listos para enviar.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Clientes | Productos | Stock | Emails de pedido |
|-----|----------|-----------|-------|-------------------|
| **A3 (Wolters Kluwer)** | Ventas → Clientes → Exportar CSV | Ventas → Artículos → Exportar | Almacén → Existencias → Exportar | Outlook: Archivo → Guardar como |
| **Sage 50 / 200** | Utilidades → Exportar → Clientes | Utilidades → Exportar → Artículos | Utilidades → Exportar → Existencias | Outlook / Gmail → carpeta compartida |
| **Holded** | Ajustes → Exportar → Contactos | Ajustes → Exportar → Productos | Ajustes → Exportar → Inventario | Gmail + Google Apps Script / N8N |
| **SAP Business One** | Consulta rápida → Socios → CSV | Consulta rápida → Artículos → CSV | Consulta rápida → Stocks → CSV | Carpeta compartida IMAP |
| **Odoo** | Contactos → Acción → Exportar | Inventario → Productos → Exportar | Inventario → Stock → Exportar | Módulo Email Gateway |

⚠️ **Nota de sector:** Este caso está diseñado para **industria y distribución mayorista B2B** (pedidos con referencias de catálogo, stock físico, descuento pactado por cliente y albarán). Funciona también en **ferretería, suministro industrial, agroalimentario mayorista y recambios**. Si tu empresa es de **servicios, hostelería o retail**, el esquema se adapta cambiando los campos de los CSVs pero la lógica es la misma. Para **gran distribución** (Mercadona, Lidl, Carrefour) que exige EDI, usa el **Caso 11 · Pedidos EDI**.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con 20 años en C-Suite. Ayudo a PYMEs españolas de **1-50M€** (industria, mayoristas y construcción) a automatizar procesos ejecutivos y traducir operaciones a impacto financiero real (EBITDA, caja, margen).

- **Diagnóstico inicial:** 750€
- **Automatización a medida:** desde 4.500€
- **Acompañamiento mensual:** 300€/mes

👉 **Reserva 30 min gratis:** [calendly.com/asesor-online-ia/30min](https://calendly.com/asesor-online-ia/30min)

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>pedidos email automático ERP, procesamiento pedidos B2B PYME, automatización administrativa mayorista, Claude Code pedidos industria, eliminar tecleo manual ERP, albarán automático email, consultor IA PYME España, OCR pedidos industriales, integración email ERP, reducir errores transcripción pedidos</sub>
