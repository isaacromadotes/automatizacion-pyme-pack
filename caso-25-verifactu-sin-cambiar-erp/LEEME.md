# Caso 25 — VERIFACTU sin cambiar de ERP

## El problema

En enero de 2027 **VERIFACTU es obligatorio** para todas las empresas en España. Tu ERP (A3, Sage, Holded, SAP, Odoo...) probablemente **todavía no está adaptado**. Las opciones son dos:

1. **Cambiar de ERP** → meses de implantación, decenas de miles de euros, parar la operativa.
2. **Añadir una capa de cumplimiento encima** → el ERP sigue como está, y Claude Code genera la factura con hash SHA-256 encadenado, firma, QR AEAT y envío automático.

Este pack muestra la **opción 2**: cumplir VERIFACTU sin tocar tu sistema. Evita sanciones de hasta **150.000 €** por factura no conforme.

---

## Qué contiene este ZIP

- `LEEME.md` → este archivo
- `prompt.txt` → el prompt que pegas en Claude Code
- `factura_venta.csv` → ejemplo de factura con 5 líneas (emisor, receptor, base 4.230 €, IVA 888,30 €, total 5.118,30 €)
- `hash_anterior.txt` → hash SHA-256 de la factura anterior para encadenar

---

## Cómo usarlo paso a paso

1. **Instala Claude Code** (si todavía no lo tienes): https://claude.com/claude-code
2. Crea una carpeta en tu equipo, por ejemplo `C:\Users\tunombre\Downloads\VERIFACTU\`
3. **Copia los 4 archivos de este ZIP** (incluido el `LEEME.md` y el `prompt.txt`) dentro de esa carpeta.
4. Abre Claude Code en esa carpeta.
5. **Arrastra el `LEEME.md` y el `prompt.txt` a la ventana de Claude Code** antes de ejecutar — así la IA entiende el contexto completo del caso.
6. Abre `prompt.txt`, cambia las variables marcadas con `[CORCHETES]` por tus datos reales (nombre de empresa, NIF, rutas).
7. Copia el prompt entero y pégalo en Claude Code. Pulsa Enter.
8. Claude Code generará: XML VERIFACTU + hash encadenado + QR AEAT + log de envío + **página web profesional de la factura**.

---

## De dónde sacar los datos en tu ERP

| ERP | Dónde está la factura emitida |
|-----|-------------------------------|
| **A3 ERP / A3 Innuva** | Facturación → Facturas emitidas → Exportar a CSV |
| **Sage 50 / 200** | Ventas → Facturas → Listado → Exportar |
| **Holded** | Ventas → Facturas → Filtrar → Exportar CSV |
| **Odoo** | Contabilidad → Clientes → Facturas → Acción → Exportar |
| **SAP Business One** | Módulo Ventas → Factura de clientes → Query manager |
| **FacturaDirecta / Quipu** | Facturas → Exportar CSV |

El **hash de la factura anterior** lo obtienes de la última factura ya firmada con VERIFACTU (si es la primera, se usa el hash vacío inicial que define la AEAT).

---

## ⚠️ Nota importante

Este prompt está diseñado para **PYMEs industriales, comerciales y de servicios** que facturan en régimen general de IVA en España. Si tu empresa opera con **régimen de recargo de equivalencia, operaciones intracomunitarias, exportaciones, o inversión del sujeto pasivo**, el campo `ClaveRegimen` del XML debe adaptarse. Indícaselo a Claude Code en el prompt.

Las facturas rectificativas, simplificadas o con retención de IRPF también requieren ajustes específicos.

---

Creado por **Isaac Romà** · https://isaacroma.com
