# Caso 11 · Procesamiento automático de pedidos EDI — Elimina 2h diarias de tecleo manual

> **Resultado clave:** Lee pedidos EDI de Mercadona, Lidl, Carrefour o DIA, los cruza con tu catálogo, valida stock y genera albaranes en segundos sin tecleo. Elimina 2h/día de administración y los errores de transcripción que generan incidencias con la gran distribución.

## 🎯 Problema que resuelve

Si tu PYME vende a gran distribución (Mercadona, Lidl, Carrefour, DIA, Alcampo, Eroski, Consum), recibes pedidos en formato **EDI (Electronic Data Interchange)** porque es el estándar obligatorio que exigen todas las grandes cadenas. El problema no es recibirlos — llegan solos por FTP/SFTP del VAN —, el problema es **procesarlos**. En la mayoría de PYMEs agroalimentarias y de bienes de consumo llegan entre 15 y 30 pedidos EDI al día; alguien del equipo administrativo abre cada fichero EDIFACT, lo interpreta a ojo y teclea manualmente cada línea en el ERP. A 5 minutos por pedido, son **más de 2 horas diarias de tecleo** que no aportan valor y que, cuando el pedido tiene 30+ líneas, disparan la probabilidad de error: EANs mal copiados, cantidades alteradas, albaranes rechazados, abonos, penalizaciones por nivel de servicio e incluso retirada de referencia por parte de la cadena. Este caso automatiza el flujo completo: lectura e interpretación del EDI (EDIFACT ORDERS D96A, EANCOM 2002 y variantes), cruce con el catálogo maestro por EAN, validación de stock disponible y precio tarifa pactado, detección de incidencias (producto no en catálogo, rotura, precio desviado) y generación automática del albarán listo para integrar en el ERP. Pensado para PYMEs agroalimentarias, de bebidas, droguería, textil o ferretería de 2-50M€ que vendan a gran distribución.

## 📦 Archivos del pack

| Archivo | Descripción |
|---------|-------------|
| `LEEME.md` | Instrucciones de uso del caso |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `csv/pedido_edi_mercadona.edi` | Ejemplo real de pedido EDIFACT ORDERS D96A |
| `csv/productos_erp.csv` | Catálogo maestro con EAN, precio tarifa y stock actual |
| `csv/clientes_erp.csv` | Ficha de cliente EDI (Mercadona) con código GLN |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** si aún no lo tienes: `npm install -g @anthropic-ai/claude-code` (requiere Node.js 18+ y cuenta Anthropic con API key). Guía oficial: [docs.anthropic.com/en/docs/claude-code](https://docs.anthropic.com/en/docs/claude-code)
2. **Copia la carpeta del pack** a tu ordenador (ej: `C:\Users\TU_USUARIO\Downloads\EDI\`) manteniendo la subcarpeta `csv/`.
3. **Abre tu terminal** (CMD, PowerShell o Terminal en Mac) y lanza `claude` desde la carpeta donde están los archivos.
4. **Pega el `prompt.txt`** y antes de pulsar Enter sustituye las variables entre corchetes por tus datos (opcional para la demo) y ajusta `@ruta/` a la ruta real de tus CSVs.
5. **Pulsa Enter y espera**. Claude Code interpreta el EDI, lo cruza con tu catálogo, valida stock y precio, detecta incidencias y abre una web local con el flujo completo: EDI bruto → pedido interpretado → albarán generado.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Catálogo productos | Ficha cliente EDI (GLN) | Pedido EDI |
|-----|---------------------|--------------------------|------------|
| **A3 (A3 ERP / A3 Innuva)** | Almacén → Listados → Exportar maestro artículos | Clientes → Datos EDI → GLN | VAN (Editran/EDICOM/SERES/Voxel/GXS) por FTP |
| **Sage 200** | Ventas y compras → Maestros → Artículos → Exportar | Clientes → Datos adicionales → GLN | Carpeta compartida del VAN |
| **Holded** | Inventario → Productos → Exportar CSV | Contactos → Campo personalizado GLN | Importar manual del VAN |
| **SAP Business One** | Inventario → Datos maestros de artículos → Exportar Excel | Socios de negocio → Datos EDI | Add-on EDI o VAN directo |
| **Odoo** | Inventario → Productos → Acción → Exportar | Contactos → Campo GLN personalizado | Módulo EDI o integración VAN |

⚠️ **Nota de sector:** Este caso está diseñado para el **sector agroalimentario, bebidas y bienes de consumo** que vende a gran distribución. El formato **EDIFACT ORDERS D96A** del ejemplo es el estándar de Mercadona, pero el prompt detecta y se adapta a variantes como **EANCOM 2002** (Carrefour, Lidl) y versiones específicas de DIA, Alcampo, Eroski y Consum. Funciona igual en **textil, ferretería y droguería** si recibes pedidos EDI — solo cambia el catálogo. En **mayorista B2B tradicional sin EDI**, usa el **Caso 02 · Pedidos por email** en su lugar.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con 20 años en C-Suite. Ayudo a PYMEs españolas de **1-50M€** (industria, mayoristas y construcción) a automatizar procesos ejecutivos y traducir operaciones a impacto financiero real (EBITDA, caja, margen).

- **Diagnóstico inicial:** 750€
- **Automatización a medida:** desde 4.500€
- **Acompañamiento mensual:** 300€/mes

👉 **Reserva 30 min gratis:** [calendly.com/asesor-online-ia/30min](https://calendly.com/asesor-online-ia/30min)

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>procesamiento EDI automático, pedidos Mercadona Lidl Carrefour DIA, EDIFACT ORDERS D96A, EANCOM 2002, automatización agroalimentaria PYME, Claude Code gran distribución, albarán EDI automático, código GLN cliente, consultor IA sector alimentario España, integración VAN ERP</sub>
