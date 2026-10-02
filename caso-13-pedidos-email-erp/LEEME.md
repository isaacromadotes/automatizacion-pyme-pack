# Caso 13 — Del email al ERP sin teclear nada

## El problema

Todos los días, alguien en tu empresa abre emails, lee pedidos y los teclea en el ERP. Uno por uno. Identifica al cliente, busca las referencias, comprueba stock, mira precio, aplica descuento, genera el pedido y el albarán. Después reenvía confirmación.

15 minutos por pedido. 20 pedidos al día. 5 horas de una persona que cuesta dinero. Y 8-10 errores de tecleo al mes que generan devoluciones, reclamaciones y facturas mal emitidas.

Este pack te muestra cómo Claude Code hace ese mismo trabajo en segundos, con cero errores.

## Qué contiene este ZIP

- **LEEME.md** — Este archivo.
- **prompt.txt** — El prompt que pegarás en Claude Code.
- **pedidos_email.csv** — 4 emails de pedido de ejemplo (clientes industriales).
- **clientes.csv** — Ficha de clientes con CIF, condiciones de pago y descuento.
- **productos.csv** — Catálogo con precio unitario e IVA.
- **stock.csv** — Existencias actuales, stock mínimo y ubicación en almacén.

## Cómo usarlo paso a paso

1. **Instala Claude Code** en tu ordenador (https://docs.claude.com/claude-code).
2. **Crea una carpeta** en tu equipo, por ejemplo `C:\Users\tu_usuario\Downloads\Caso 13 Pedidos ERP\`.
3. **Copia los 4 CSVs** de este ZIP a esa carpeta.
4. **Abre la terminal** (iTerm en Mac, PowerShell en Windows) y escribe `claude` para arrancar Claude Code.
5. **Arrastra dentro de la terminal** el archivo `LEEME.md` y el `prompt.txt` de este ZIP — así Claude Code entiende el contexto antes de ejecutar.
6. **Abre `prompt.txt`**, cambia las variables `[EMPRESA]`, `[MES AÑO]` y la ruta `@ruta/` por tus datos reales y pega el contenido en Claude Code.
7. **Pulsa Enter** y espera. Claude Code procesará los pedidos y arrancará una web local con el resultado.

## De dónde sacar estos datos en tu ERP

- **A3 (Wolters Kluwer):** Módulo Ventas → Exportar clientes, artículos y stock a Excel/CSV.
- **Sage 50 / 200:** Utilidades → Exportar → Clientes, Artículos, Existencias.
- **Holded:** Ajustes → Exportar datos → Contactos, Productos, Inventario.
- **SAP Business One:** Herramientas → Consultas → Consulta rápida → guardar como CSV.
- **Odoo:** Cada módulo (Contactos, Inventario, Ventas) permite Exportar desde el menú de acciones.
- **Los emails de pedido** los exporta tu cliente de correo (Outlook: Archivo → Guardar como; Gmail: reenviar a un buzón y usar Google Apps Script, o usar N8N/Zapier para volcar el asunto y cuerpo a un CSV).

## Nota importante

Este prompt está diseñado para **industria y distribución mayorista** (pedidos B2B con referencias, stock físico y albarán). Si trabajas en otro sector (servicios, hostelería, retail), el esquema se adapta cambiando los campos del CSV, pero la lógica es la misma: leer una entrada de texto libre → cruzar con maestros → validar → generar entregable estructurado.

---

Creado por Isaac Romà · https://isaacroma.com
