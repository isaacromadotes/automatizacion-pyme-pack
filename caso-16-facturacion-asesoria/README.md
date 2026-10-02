# Caso 16 · Facturación masiva de asesoría — De 2 días a minutos

> Gestoría con **400 clientes**, cierre mensual: pasa de **2 días completos** facturando a **minutos**, con remesa SEPA 19.14 lista para el banco.

## 🎯 Problema que resuelve

En una gestoría o asesoría con 400 clientes, el fin de mes es el fin de mes: un socio o un administrativo se tira dos días completos calculando honorarios cliente a cliente, generando facturas una a una, preparando la remesa SEPA para el banco y mandando los emails con el PDF adjunto. Es el mes que no se factura trabajo nuevo porque se está facturando el anterior, y cualquier error en un IBAN o en un extra se detecta cuando el banco devuelve el recibo o cuando el cliente llama cabreado. El modelo típico de despacho profesional español combina cuota mensual recurrente más servicios extras (una renta, una herencia, una inspección, un modelo puntual), y ese pequeño componente variable es lo que convierte el proceso en manual y propenso a fallos. Este pack lo automatiza entero con un solo prompt: Claude Code lee el maestro de clientes con cuotas y extras, calcula honorarios, genera las facturas en HTML optimizadas para visualización vertical 9:16, prepara los emails de envío al cliente, monta la remesa SEPA en XML según norma 19.14 (pain.008.001.02) lista para subir al banco y entrega un Excel resumen con totales, detalle por cliente e incidencias (IBAN inválido, email vacío, cuota a cero). Dos días de trabajo administrativo repetitivo convertidos en una ejecución que revisas, firmas y envías.

## 📦 Archivos del pack

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Documento inicial con la explicación del caso. |
| `prompt.txt` | Prompt listo para pegar en Claude Code. |
| `clientes.csv` | 400 clientes ficticios de "Asesoría Martínez y Asociados" con NIF, IBAN, email, cuota mensual, extras y forma de pago (total 127.840 €). |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la [documentación oficial](https://docs.anthropic.com/en/docs/claude-code): `npm install -g @anthropic-ai/claude-code`
2. **Descomprime este pack** en una carpeta local (ej. `C:\Facturacion_Asesoria\`) y abre la terminal dentro con el comando `claude`.
3. **Arrastra a la ventana de Claude Code** el `LEEME.md`, el `prompt.txt` y el `clientes.csv` para que tenga todo el contexto.
4. **Copia el contenido de `prompt.txt`**, pégalo en Claude Code y sustituye `[EMPRESA]` y `[MES AÑO]` por tus datos (o déjalos por defecto para probar con la demo).
5. **Pulsa Enter**: Claude Code genera 3 facturas HTML de ejemplo (1080×1920), 3 emails HTML de ejemplo, la remesa SEPA XML pain.008.001.02 lista para subir al banco y un Excel resumen con totales, detalle por cliente e incidencias.

## 🔌 Cómo exportar los datos desde tu ERP

| Dato | A3ASESOR (Wolters Kluwer) | Sage 50 / Despachos | Holded | SAP Business One | Odoo | Contasol / ContaPlus |
|---|---|---|---|---|---|---|
| Maestro de clientes (NIF, IBAN, email, forma de pago) | Facturación → Maestros → Clientes → Exportar Excel | Ficheros → Clientes → Utilidades → Exportar | Contactos → Filtro "clientes" → Exportar CSV | Business Partners → Query Manager (CardCode, LicTradNum, IBAN, MailAddress) | Contactos → Filtros: Cliente → Acción → Exportar | Ficheros → Clientes → Listado → Exportar Excel |
| Cuotas y extras del mes | Añadir columnas `cuota_mensual` y `extras_importe` desde hoja de honorarios o módulo de iguala | Módulo de iguala / cuotas periódicas → Exportar | Facturas recurrentes → Exportar | Contratos de servicios → Query | Suscripciones → Exportar | Hoja auxiliar de honorarios → Añadir columnas al CSV |

> ⚠️ **Nota de sector:** este pack está diseñado específicamente para **gestorías, asesorías y despachos profesionales españoles** que facturan cuota mensual recurrente más extras. Si tu modelo es por horas, por proyecto o por producto, el cálculo y el layout necesitan ajustes. La remesa SEPA sigue la norma **19.14 (pain.008.001.02)**: verifica con tu banco si usa esquema **CORE o B2B** antes de pasar a producción. Para completar el ciclo de cobro combina con el [caso-04 (facturas)](../caso-04-facturas/) y el [caso-08 (control de DSO y cobros)](../caso-08-cobros-dso/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años en C-Suite.
Ayudo a **PYMEs industriales, mayoristas y de construcción (1-50M€)** a automatizar operaciones y recuperar margen con IA aplicada al negocio real, no a la tecnología.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **Automatización a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min conmigo:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>facturación masiva asesoría automática, remesa sepa 19.14 asesoría, facturar gestoría cuotas mensuales, automatizar facturación despacho profesional, pain.008.001.02 adeudos directos, generar facturas asesoría en lote, cerrar mes gestoría en minutos, software facturación asesoría pyme, honorarios recurrentes más extras, remesa bancaria clientes despacho</sub>
