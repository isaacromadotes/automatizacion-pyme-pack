# Caso 24 · Propuestas comerciales en 2 horas — De 2 días a 2 horas por propuesta

> 3 propuestas/semana = **6 días de un comercial senior cada semana** copiando y maquetando. Pasa a 2 horas por propuesta con calidad consultora.

## 🎯 Problema que resuelve

En una consultora, agencia o empresa de servicios B2B, cada propuesta nueva se monta igual: el comercial coge la última propuesta que envió, borra lo que no aplica, busca los datos del prospecto en el CRM o en LinkedIn, rebusca entre los casos de éxito del año cuáles se parecen más al sector del prospecto, abre el catálogo de pricing, maqueta todo en Word o Google Docs, exporta a PDF y escribe el email de presentación. Dos días completos de un comercial senior por cada propuesta, y lo que sale al final es una propuesta genérica con sabor a plantilla que no diferencia nada y que compite por precio porque no transmite valor específico para ese prospecto. Multiplicado por 3 propuestas semanales son 6 días de capacidad comercial consumidos solo en maquetación mientras la tasa de conversión se mantiene mediocre porque nada en el documento habla directamente del problema del cliente. Este pack resuelve el ciclo entero con un flujo de 4 inputs: datos del prospecto, plantilla base, casos de éxito del año y paquetes de pricing. Claude Code lee los 5 casos de éxito disponibles, selecciona los 2 más afines al sector y tamaño del prospecto, redacta un diagnóstico sectorial específico, define el scope en 3 fases, monta la tabla de pricing con la opción recomendada destacada, maqueta la propuesta como web autocontenida con nivel visual de consultora grande y entrega además el email de presentación listo para enviar. De 2 días a 2 horas con mejor personalización, por tanto mejor tasa de cierre.

## 📦 Archivos del pack

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Documento inicial con la explicación del caso. |
| `prompt.txt` | Prompt listo para pegar en Claude Code. |
| `prospecto.csv` | Datos del prospecto (ficticio: Distribuidora Costa S.L.). |
| `plantilla_propuesta.md` | Estructura base de la propuesta en markdown. |
| `casos_exito.csv` | 5 casos de éxito ficticios para que Claude elija los 2 más afines. |
| `servicios_pricing.csv` | 3 paquetes con scope y precio. |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la [documentación oficial](https://docs.anthropic.com/en/docs/claude-code): `npm install -g @anthropic-ai/claude-code`
2. **Descomprime este pack** en una carpeta local (ej. `C:\Propuestas\`) y abre la terminal dentro con el comando `claude`.
3. **Arrastra a la ventana de Claude Code** el `LEEME.md`, el `prompt.txt` y los 4 archivos de datos para que tenga todo el contexto.
4. **Copia el contenido de `prompt.txt`**, pégalo en Claude Code y sustituye `[EMPRESA]`, `[MES AÑO]` y `[RUTA]` por tus datos reales.
5. **Pulsa Enter**: en 2-3 minutos Claude Code entrega en `output/` la `propuesta.html` (nivel visual consultora), la `propuesta.pdf` lista para enviar y el `email_presentacion.txt` para pegar en Outlook o Gmail.

## 🔌 Cómo exportar los datos desde tu CRM / ERP

| Dato | HubSpot | Pipedrive | Salesforce | Zoho | Odoo CRM | Holded |
|---|---|---|---|---|---|---|
| Datos del prospecto | Contactos / Empresas → Exportar propiedades | Personas / Organizaciones → Exportar | Leads / Accounts → Report Builder → Exportar | Leads → Vista → Exportar | CRM → Pipeline → Exportar | CRM → Contactos → Exportar |
| Casos de éxito (oportunidades ganadas) | Deals → Filtro "Closed Won" → Exportar | Deals → Estado "Won" → Exportar | Opportunities → Stage "Closed Won" → Exportar | Deals → Won → Exportar | Oportunidades → Ganadas → Exportar | Pipeline → Ganadas → Exportar |
| Pricing / catálogo de servicios | Products → Exportar | Products → Exportar | Products / Price Books → Exportar | Products → Exportar | Productos de servicio → Exportar | Servicios → Exportar |
| Plantilla base | Última propuesta enviada → convertir a markdown | ídem | ídem | ídem | ídem | ídem |

> ⚠️ **Nota de sector:** este pack está pensado para **servicios de consultoría a PYMEs españolas (1-50M€)** y venta B2B basada en propuesta a medida (agencias, ingenierías, estudios de arquitectura, despachos profesionales, servicios técnicos). Si vendes productos físicos, SaaS por suscripción o servicios recurrentes, cambia la estructura del scope y la plantilla; el flujo (prospecto + casos + pricing → web + email) se mantiene. Para completar el ciclo comercial, combina con el [caso-16 (facturación masiva asesoría)](../caso-16-facturacion-asesoria/) y el [caso-18 (cuadro de mando con aprobaciones)](../caso-18-cuadro-mando-aprobaciones/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años en C-Suite.
Ayudo a **PYMEs industriales, mayoristas y de construcción (1-50M€)** a automatizar operaciones y recuperar margen con IA aplicada al negocio real, no a la tecnología.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min conmigo:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>propuesta comercial automática consultora, generar propuesta b2b en 2 horas, propuesta personalizada por sector pyme, casos de éxito seleccionados por afinidad, plantilla propuesta consultora html pdf, automatizar propuestas comerciales crm, tasa de cierre propuesta b2b, email de presentación propuesta cliente, propuesta nivel consultora grande pyme, reducir tiempo propuesta comercial</sub>
