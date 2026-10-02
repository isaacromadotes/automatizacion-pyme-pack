# Caso 11 — Procesamiento automático de pedidos EDI

## El problema

Si tu empresa vende a Mercadona, Lidl, Carrefour, DIA o cualquier gran cadena de distribución, recibes pedidos en formato **EDI** (Electronic Data Interchange). Es el estándar que usan todas las grandes cuentas.

El problema no es recibirlos. El problema es **procesarlos**.

En la mayoría de PYMEs agroalimentarias:

- Llegan 15–30 pedidos EDI al día
- Alguien del equipo administrativo abre cada fichero, lo interpreta y **teclea a mano** cada línea en el ERP
- Tarda unos 5 min por pedido → **2h diarias tecleando**
- Cada tecleo es un riesgo de error de transcripción (EAN mal copiado, cantidad de más/menos)
- Cuando el pedido tiene 30 líneas, la probabilidad de error se dispara

Este pack demuestra cómo Claude Code lee el EDI, lo cruza con tu catálogo, valida stock y genera el albarán. En segundos, sin tocar el teclado.

## Qué contiene el ZIP

- `LEEME.md` — Este documento
- `prompt.txt` — El prompt a pegar en Claude Code
- `csv/pedido_edi_mercadona.edi` — Ejemplo de pedido EDI real (formato EDIFACT ORDERS D96A)
- `csv/productos_erp.csv` — Catálogo maestro de productos del ERP con stock actual
- `csv/clientes_erp.csv` — Ficha de cliente en el ERP (Mercadona)

## Cómo usarlo

1. **Instala Claude Code** en tu ordenador → https://claude.ai/download
2. **Copia esta carpeta completa** a un sitio accesible (por ejemplo `C:\Users\tunombre\Downloads\Caso11\`)
3. **Abre la terminal** en esa carpeta
4. **Escribe `claude`** y pulsa Enter
5. **Arrastra este LEEME.md y el prompt.txt** a la ventana de Claude Code para que tenga contexto completo
6. **Abre `prompt.txt`**, cambia las variables entre corchetes por tus datos (opcional para la demo) y pega el prompt
7. **Pulsa Enter** y deja que Claude Code trabaje
8. Cuando termine, abrirá una web local con el flujo completo: EDI bruto → pedido interpretado → albarán generado

## De dónde sacar tus datos reales

Si quieres probarlo con tus propios pedidos:

- **Fichero EDI**: te lo entrega tu proveedor de VAN (Editran, EDICOM, Voxel, SERES, GXS). Suele llegar por FTP o SFTP a una carpeta compartida
- **Catálogo de productos**: expórtalo de tu ERP como CSV con estas columnas mínimas: `codigo_interno`, `ean`, `descripcion`, `precio_tarifa`, `stock_actual`
  - **A3 ERP**: Módulo Almacén → Listados → Exportar maestro de artículos
  - **Sage 200**: Ventas y compras → Maestros → Artículos → Exportar
  - **Holded**: Inventario → Productos → Exportar CSV
  - **SAP Business One**: Inventario → Datos maestros de artículos → Exportar Excel
  - **Odoo**: Inventario → Productos → Acción → Exportar
- **Ficha de cliente**: normalmente ya la tienes cargada en el ERP con el código GLN de la cadena (obligatorio para EDI)

## Nota importante

Este prompt está diseñado para el **sector agroalimentario que vende a gran distribución**. El formato EDIFACT ORDERS D96A que aparece en el ejemplo es el estándar que usa Mercadona, pero funciona igual para Lidl, Carrefour, DIA, Alcampo, Eroski y Consum. Si tu cadena usa una variante ligeramente distinta (por ejemplo EANCOM 2002), el prompt sigue funcionando — Claude Code detecta el formato y se adapta.

Si tu empresa no está en agroalimentario pero recibe pedidos EDI (textil, ferretería, droguería), el prompt también sirve. Solo tienes que reemplazar los productos del CSV por los tuyos.

---

**Creado por Isaac Romà · https://isaacroma.com**
