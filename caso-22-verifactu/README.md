# Caso 22 · Factura certificada VERIFACTU — Cumple el RD 1007/2023 en minutos

> **1 enero 2027: VERIFACTU obligatorio** para todos los sistemas de facturación en España. **79% de las PYMEs** aún no están adaptadas. Factura certificada completa (XML + hash encadenado + QR + envío AEAT) generada en minutos.

## 🎯 Problema que resuelve

A partir del 1 de enero de 2027, el Real Decreto 1007/2023 obliga a todos los sistemas de facturación en España a emitir facturas verificables (VERIFACTU), con requisitos técnicos muy concretos: cada factura debe incluir un XML con el formato oficial AEAT, un hash SHA-256 encadenado con la factura anterior para garantizar inalterabilidad, un código QR de verificación que permita al receptor comprobar la factura en la sede electrónica, y un canal de envío a la AEAT. Según los datos de mercado, cerca del 79% de las PYMEs españolas aún no están adaptadas, y la vía habitual (comprar o actualizar un software de facturación certificado) cuesta varios miles de euros, lleva meses de implantación y choca con la realidad de la micropyme y el autónomo profesional, que no tiene ni presupuesto ni margen operativo para una migración. Para asesores y gestores, esto significa que cientos de clientes de su cartera llegan a 2027 sin cumplir y sin una solución asequible que ofrecer. Este pack resuelve el problema con una capa ligera sobre Claude Code: dados los datos de factura, el hash de la factura anterior y el certificado digital, genera el XML con todos los campos obligatorios del RD 1007/2023, calcula el hash encadenado, crea el QR de verificación AEAT, simula el envío al servicio web de Hacienda y entrega la factura final en HTML y PDF. Un flujo que un asesor puede operar por decenas de clientes a coste marginal.

## 📦 Archivos del pack

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Documento inicial con la explicación del caso. |
| `prompt.txt` | Prompt listo para pegar en Claude Code. |
| `factura_cliente.csv` | Datos de la factura de ejemplo (emisor, receptor, 3 líneas con IVA). |
| `hash_anterior.txt` | Hash SHA-256 de la factura anterior (necesario para el encadenamiento). |
| `certificado_firma.txt` | Datos del certificado digital simulado. |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la [documentación oficial](https://docs.anthropic.com/en/docs/claude-code): `npm install -g @anthropic-ai/claude-code`
2. **Descomprime este pack** en una carpeta local (ej. `C:\VERIFACTU\`) y abre la terminal dentro con el comando `claude`.
3. **Arrastra a la ventana de Claude Code** el `LEEME.md`, el `prompt.txt`, el CSV de factura y los 2 .txt (hash y certificado) para que tenga todo el contexto.
4. **Copia el contenido de `prompt.txt`**, pégalo en Claude Code y sustituye `[EMPRESA]`, `[MES AÑO]` y `@ruta/` por tus datos reales.
5. **Pulsa Enter**: Claude Code valida la factura, genera el XML según RD 1007/2023, calcula el hash SHA-256 encadenado, crea el QR de verificación AEAT, simula el envío a Hacienda y entrega la factura en HTML y PDF.

## 🔌 Cómo exportar los datos desde tu ERP

| Dato | A3 | Sage | Holded | SAP Business One | Odoo | Contasol / Sage Despachos / ContaPlus |
|---|---|---|---|---|---|---|
| Datos de factura (emisor, receptor, líneas, IVA) | Gestión de Ventas → Facturas emitidas → Exportar detalle | Ventas → Facturas → Exportar CSV/Excel | Ventas → Facturas → Exportar | Gestión de ventas → Factura de deudores → Exportar | Contabilidad → Facturas de cliente → Exportar | Gestión → Facturas emitidas → Listado → Exportar |
| Hash de la factura anterior | Guardar `hash_actual.txt` tras cada emisión y renombrar como `hash_anterior.txt` para la siguiente | ídem | ídem | ídem | ídem | ídem |
| Certificado digital | Certificado FNMT / Camerfirma / Izenpe instalado localmente o en HSM | ídem | ídem | ídem | ídem | ídem |

> ⚠️ **Nota de sector:** este pack está pensado para **asesorías, gestorías, despachos profesionales y cualquier PYME o autónomo** sujeto al RD 1007/2023 (VERIFACTU) a partir del 1 de enero de 2027. La **simulación de envío a AEAT es demostrativa**: en producción se requiere certificado digital válido, conexión al servicio web oficial de la Agencia Tributaria y verificación legal del circuito completo. Para completar el ciclo de facturación en una asesoría, combina con el [caso-04 (facturas)](../caso-04-facturas/), el [caso-10 (vencimientos fiscales)](../caso-10-vencimientos-fiscales/) y el [caso-16 (facturación masiva asesoría)](../caso-16-facturacion-asesoria/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años en C-Suite.
Ayudo a **PYMEs industriales, mayoristas y de construcción (1-50M€)** a automatizar operaciones y recuperar margen con IA aplicada al negocio real, no a la tecnología.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min conmigo:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>verifactu factura certificada rd 1007/2023, cumplir verifactu pyme 2027, factura con hash sha-256 encadenado, qr verificación aeat factura, xml facturación aeat obligatorio, software verifactu barato asesoría, adaptar facturación verifactu autónomo, suministro inmediato información facturas, verifactu gestoría clientes masivo, factura electrónica aeat 2027</sub>
