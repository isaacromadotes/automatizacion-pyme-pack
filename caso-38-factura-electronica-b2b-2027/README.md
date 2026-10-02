# Caso 38 · Factura electrónica B2B obligatoria en 2027 — Clasifica cartera y genera EDI, Facturae y PDF desde un único origen

> **Resultado:** Clasificación automática de los 200 clientes de la cartera por formato exigido (EDI / Facturae / PDF), generación de ejemplo de factura en los 3 formatos y web local que lo muestra todo. Preparación real para la Ley Crea y Crece sin esperar a última hora.

## 🎯 Problema que resuelve

En 2027 la factura electrónica entre empresas (B2B) será obligatoria en España por la Ley Crea y Crece, y toda PYME que facture a otras empresas tendrá que emitir en formato electrónico estructurado. El problema no es la obligación en sí sino la fragmentación de formatos que exigirá la cartera real: las grandes cuentas (Carrefour, Leroy Merlin, Bricomart, Mercadona, El Corte Inglés) ya exigen EDI INVOIC D96A por AS2 o SFTP con códigos EAN propios; las medianas piden Facturae 3.2.2 (XML firmado con certificado) por email, portal propio o plataforma intermedia; las pequeñas siguen aceptando (y en muchos casos prefiriendo) PDF simple por email hasta que la norma les obligue también. El resultado es que la administración de una PYME mayorista o industrial trabaja ya hoy con tres flujos distintos, cada cliente tiene su particularidad (puerto SFTP, estructura de archivo, códigos internos del comprador) y a pocos meses de la obligatoriedad el gerente no sabe por dónde empezar: contratar una plataforma externa, invertir en el ERP, delegar en el proveedor logístico o esperar. Este caso automatiza la clasificación de la cartera completa por formato exigido cruzando criterios objetivos (volumen anual facturado, sector, existencia de portal de proveedores, presencia histórica en EDI), genera un ejemplo real de la misma factura en los tres formatos (EDI INVOIC, Facturae 3.2.2 XML y PDF estructurado) y entrega una web local donde el gerente ve de un vistazo qué porcentaje de la facturación va por cada canal y qué clientes requieren acción prioritaria.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `factura.csv` | 10 facturas base de ejemplo (Suministros Levante S.L., ficticia) |
| `clientes_efactura.csv` | 200 clientes ficticios clasificados por formato (EDI / Facturae / PDF) y canal de envío |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_38_eFactura\`) con los 2 CSVs en la raíz.
3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md`, `prompt.txt` y los 2 CSVs** al chat para dar contexto antes de ejecutar.
5. **Edita `prompt.txt`** cambiando `[EMPRESA]`, `[MES AÑO]` y las rutas `@ruta/`, pégalo y pulsa Enter. Obtendrás clasificación de los 200 clientes, ejemplo en EDI + Facturae + PDF y web local navegable.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Cartera clientes con canal / formato |
|---|---|
| **A3 ERP (Wolters Kluwer)** | Clientes → Export CSV con CIF, canal de facturación y formato preferente |
| **Sage 50 / Sage 200** | Mantenimiento → Clientes → Listado personalizado → Export Excel |
| **Holded** | Contactos → Clientes → Export CSV |
| **SAP Business One** | Business Partners → Query Generator → Export Excel |
| **Odoo** | Contactos → Filtro tipo "Empresa" → Export |
| **Navision / Business Central** | Clientes → Vista personalizada → Export |
| **Factusol** | Archivo → Exportar → Clientes |
| **Contasol / ContaPlus** | Maestros → Clientes → Export CSV |

Si tu ERP no tiene el campo "formato de factura electrónica", el prompt genera también una **matriz de criterios de clasificación** (por volumen anual facturado, sector, existencia de portal de proveedores, histórico EDI) para que la administración complete la clasificación en pocas horas.

> ⚠️ **Nota de sector:** Diseñado para **PYMEs B2B con cartera mixta de clientes** (grandes + medianas + pequeñas). Aplica especialmente a **mayoristas y distribución, fabricantes con red comercial B2B, suministros industriales, material de construcción y alimentación a canal HORECA**. Si solo facturas a particulares (B2C puro) o solo a Administración Pública (Facturae ya obligatorio desde hace años por FACE), el flujo es más simple y este caso es sobredimensionado. Para enlazar con el impacto en caja del cambio normativo, combina con [caso-32 (forecast tesorería mayorista)](../caso-32-forecast-tesoreria-mayorista/) para anticipar efectos sobre el DSO durante la transición.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>factura electrónica B2B obligatoria 2027, Ley Crea y Crece PYME, EDI INVOIC D96A gran distribución, Facturae 3.2.2 XML firmado, clasificación cartera formato efactura, Claude Code factura electrónica, mayoristas obligación efactura España, portal proveedores Carrefour Leroy Merlin, automatización administración facturación B2B, consultoría transformación digital PYME mayorista</sub>
