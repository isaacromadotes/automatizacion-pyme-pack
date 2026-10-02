# Caso 25 · VERIFACTU sin cambiar de ERP — Capa de cumplimiento sobre tu sistema actual

> Enero 2027: **VERIFACTU obligatorio**. Sanciones de hasta **150.000 €** por factura no conforme. Cumple sin tocar tu ERP ni gastar en migración.

## 🎯 Problema que resuelve

El RD 1007/2023 obliga desde el 1 de enero de 2027 a que toda factura emitida en España pase por el régimen VERIFACTU: XML con el formato oficial AEAT, hash SHA-256 encadenado con la factura anterior, firma, código QR de verificación y envío al servicio web de la Agencia Tributaria. Las sanciones alcanzan los 150.000 € por factura no conforme. El problema real para la mayoría de PYMEs es que su ERP (A3, Sage 50/200, Holded, SAP Business One, Odoo, FacturaDirecta, Quipu) o bien no está adaptado todavía o bien ofrece una actualización cara que exige migración, formación y parar la operativa en el peor momento del año. La respuesta habitual del mercado (cambiar de ERP) significa meses de implantación y decenas de miles de euros que la micropyme y la pyme pequeña no pueden absorber. Este pack muestra la vía alternativa: una capa de cumplimiento ligera sobre el ERP actual. El sistema sigue facturando como siempre y exportando sus facturas en CSV; Claude Code recoge la factura exportada, construye el XML con todos los campos obligatorios, calcula el hash encadenado con la factura anterior, genera el QR de verificación AEAT, registra el envío al servicio web de Hacienda y entrega la factura firmada en una página web profesional lista para enviar al cliente. Cero migración, cero parada de operativa, coste marginal por factura y cumplimiento legal garantizado desde el día uno.

## 📦 Archivos del pack

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Documento inicial con la explicación del caso. |
| `prompt.txt` | Prompt listo para pegar en Claude Code. |
| `factura_venta.csv` | Factura de ejemplo con 5 líneas (base 4.230 €, IVA 888,30 €, total 5.118,30 €). |
| `hash_anterior.txt` | Hash SHA-256 de la factura anterior para encadenar. |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la [documentación oficial](https://docs.anthropic.com/en/docs/claude-code): `npm install -g @anthropic-ai/claude-code`
2. **Descomprime este pack** en una carpeta local (ej. `C:\VERIFACTU_ERP\`) y abre la terminal dentro con el comando `claude`.
3. **Arrastra a la ventana de Claude Code** el `LEEME.md`, el `prompt.txt`, el CSV de factura y el `hash_anterior.txt` para que tenga todo el contexto.
4. **Copia el contenido de `prompt.txt`**, pégalo en Claude Code y sustituye las variables entre corchetes (empresa, NIF, rutas) por tus datos reales.
5. **Pulsa Enter**: Claude Code genera el XML VERIFACTU, el hash SHA-256 encadenado, el QR de verificación AEAT, el log de envío y la página web profesional de la factura.

## 🔌 Cómo exportar los datos desde tu ERP

| Dato | A3 ERP / A3 Innuva | Sage 50/200 | Holded | SAP Business One | Odoo | FacturaDirecta / Quipu |
|---|---|---|---|---|---|---|
| Factura emitida (líneas, base, IVA, total) | Facturación → Facturas emitidas → Exportar CSV | Ventas → Facturas → Listado → Exportar | Ventas → Facturas → Filtrar → Exportar CSV | Ventas → Factura de clientes → Query Manager | Contabilidad → Clientes → Facturas → Acción → Exportar | Facturas → Exportar CSV |
| Hash de la factura anterior | Última factura firmada con VERIFACTU (o hash inicial vacío definido por AEAT si es la primera) | ídem | ídem | ídem | ídem | ídem |

> ⚠️ **Nota de sector:** este pack está diseñado para **PYMEs industriales, comerciales y de servicios** en régimen general de IVA en España. Si operas en **recargo de equivalencia, operaciones intracomunitarias, exportaciones o inversión del sujeto pasivo**, el campo `ClaveRegimen` del XML debe adaptarse (indícalo a Claude Code en el prompt). Las facturas **rectificativas, simplificadas o con retención de IRPF** requieren ajustes específicos. Para el ciclo completo de facturación y VERIFACTU, combina con el [caso-04 (facturas)](../caso-04-facturas/), el [caso-16 (facturación masiva asesoría)](../caso-16-facturacion-asesoria/) y el [caso-22 (VERIFACTU estándar)](../caso-22-verifactu/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años en C-Suite.
Ayudo a **PYMEs industriales, mayoristas y de construcción (1-50M€)** a automatizar operaciones y recuperar margen con IA aplicada al negocio real, no a la tecnología.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min conmigo:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>verifactu sin cambiar erp, capa cumplimiento verifactu a3 sage holded, cumplir rd 1007/2023 sin migración, verifactu sobre erp actual pyme, evitar sanción 150000 factura verifactu, xml verifactu hash encadenado qr aeat, verifactu sap odoo facturadirecta quipu, factura verifactu capa adicional, cumplimiento verifactu enero 2027 pyme, verifactu barato autónomo gestoría</sub>
