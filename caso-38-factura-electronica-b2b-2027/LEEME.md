# Caso 38 — Factura electrónica B2B obligatoria en 2027

## El problema

En 2027 la factura electrónica entre empresas (B2B) será obligatoria en España (Ley Crea y Crece). Si tu empresa factura a otras empresas, tienes que emitir en formato electrónico estructurado.

El dolor real: **tus clientes NO piden todos el mismo formato**.
- Las grandes cuentas (Carrefour, Leroy Merlin, Bricomart…) exigen **EDI** (INVOIC D96A) por AS2 o SFTP.
- Las medianas piden **Facturae 3.2.2** (XML firmado) por email o portal.
- Las pequeñas aún tiran de **PDF** por email.

Resultado: tu administración trabaja con 3 flujos distintos, cada cliente tiene su particularidad, y a 3 meses de la obligatoriedad nadie en la empresa sabe por dónde empezar.

Este caso te muestra cómo clasificar tu cartera y generar los 3 formatos desde un único origen, con Claude Code, en una sola conversación.

## Qué contiene este ZIP

- **LEEME.md** — este archivo
- **prompt.txt** — el prompt que vas a pegar en Claude Code
- **factura.csv** — 10 facturas base de ejemplo (empresa ficticia: Suministros Levante S.L.)
- **clientes_efactura.csv** — 200 clientes ficticios ya clasificados por formato (EDI / Facturae / PDF) y canal de envío

## Cómo usarlo (5 minutos)

1. **Instala Claude Code** si no lo tienes → https://claude.ai/code
2. **Copia los CSVs** a una carpeta de tu ordenador. Ejemplo: `C:\e-factura\` o `~/Descargas/e-factura/`
3. **Abre la terminal** (iTerm en Mac, PowerShell en Windows) y escribe `claude`
4. **Abre `prompt.txt`**, cambia la ruta de los `@...` por la tuya, y pégalo en Claude Code
5. **Enter.** Claude Code lee los CSVs, clasifica los 200 clientes, genera un ejemplo de factura en los 3 formatos (EDI INVOIC, Facturae XML, PDF) y monta una web local que lo muestra todo

Variables que debes cambiar antes de ejecutar:
- `[EMPRESA]` → nombre de tu empresa
- `[MES AÑO]` → mes y año del ejercicio (ej: enero 2027)
- `@ruta/` → la carpeta real donde pusiste los CSVs

## De dónde sacar los datos reales en tu ERP

- **A3 / A3ERP** → Clientes → Exportar → CSV con CIF, canal de facturación, formato preferente
- **Sage 50 / Sage 200** → Mantenimiento → Clientes → Listado personalizado → Exportar a Excel
- **Holded** → Contactos → Clientes → Exportar CSV
- **SAP Business One** → Business Partners → Query Generator → exportar a Excel
- **Odoo** → Contactos → filtrar por tipo "Empresa" → Exportar
- **Factusol** → Archivo → Exportar → Clientes

Si tu ERP no tiene el campo "formato de factura electrónica", el prompt también te genera una **matriz de criterios** para que clasifiques tú (por volumen anual, por sector, por si tiene o no portal de proveedores).

## Nota importante

Este caso está diseñado para **empresas B2B con cartera mixta de clientes** (grandes + medianas + pequeñas). Si solo facturas a particulares (B2C) o solo a Administración Pública (donde Facturae ya es obligatorio desde hace años), el flujo es distinto y mucho más simple.

Sectores donde este caso aplica especialmente:
- Mayoristas y distribución
- Fabricantes con red comercial B2B
- Suministros industriales
- Material de construcción
- Alimentación a canal HORECA

---

Creado por Isaac Romà · https://isaacroma.com
