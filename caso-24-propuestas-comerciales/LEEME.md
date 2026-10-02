# CASO 24 — Propuestas comerciales en 2 horas (en vez de 2 días)

## El problema

Cada vez que llega un prospecto, tu equipo comercial pierde **2 días completos** montando la propuesta:
copiar la última que se envió, borrar lo que no aplica, buscar datos del cliente,
rebuscar casos de éxito similares en el CRM, maquetar en Word, exportar a PDF…
Y al final sale una propuesta genérica, con sabor a plantilla, que no diferencia nada.

**Coste real:** si envías 3 propuestas a la semana, son **6 días de un comercial senior cada semana**.
Y la tasa de cierre no mejora, porque la propuesta no está personalizada de verdad.

## La solución

Le das a Claude Code 4 archivos:
- Los **datos del prospecto** (una fila con empresa, sector, facturación, problema)
- Tu **plantilla** base de propuesta (estructura con las secciones de siempre)
- Tus **casos de éxito** (el CRM exportado o el Excel donde los llevas)
- Tus **paquetes de pricing** (los 3 niveles que ofreces)

Y Claude Code genera una **propuesta web espectacular** (nivel Baker McKenzie, McKinsey)
en HTML autocontenido: portada personalizada, diagnóstico sectorial, scope en 3 fases,
tabla de pricing con opción recomendada destacada, 2 casos de éxito seleccionados por
afinidad al prospecto, equipo, condiciones. Más el **email de presentación** listo para enviar.

**De 2 días → 2 horas.** Más propuestas enviadas, mejor tasa de cierre.

## Qué contiene este ZIP

- `LEEME.md` — este archivo
- `prompt.txt` — el prompt que pegarás en Claude Code
- `prospecto.csv` — datos del prospecto (ficticio: Distribuidora Costa S.L.)
- `plantilla_propuesta.md` — estructura base de la propuesta
- `casos_exito.csv` — 5 casos de éxito (ficticios) para que Claude elija los 2 más parecidos
- `servicios_pricing.csv` — tus 3 paquetes con scope y precio

## Cómo usarlo (paso a paso)

1. **Instala Claude Code** si no lo tienes: `npm install -g @anthropic-ai/claude-code` (necesitas Node.js).
2. **Descomprime este ZIP** en una carpeta, por ejemplo `C:\Users\tunombre\Downloads\caso_24\`.
3. **Abre terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra a la ventana de Claude Code** estos 3 archivos para que los lea de contexto:
   `LEEME.md`, `prompt.txt` y los 4 CSVs. Así la IA entiende qué va a hacer antes de ejecutar.
5. **Abre `prompt.txt`**, cambia las variables entre corchetes `[EMPRESA]`, `[MES AÑO]`, `[RUTA]`
   por tus datos reales (o déjalas con los datos de ejemplo si solo quieres probar).
6. **Pega el prompt** en Claude Code y pulsa Enter.
7. En 2–3 minutos tendrás en la carpeta `output/`:
   - `propuesta.html` — la propuesta web espectacular (ábrela en Chrome)
   - `propuesta.pdf` — misma propuesta exportada a PDF para enviar
   - `email_presentacion.txt` — email listo para pegar en Outlook/Gmail

## De dónde sacar los datos reales en tu ERP/CRM

- **prospecto.csv** → de tu CRM (HubSpot, Pipedrive, Salesforce, Zoho) o del formulario de contacto web.
  También vale una ficha de LinkedIn Sales Navigator.
- **casos_exito.csv** → exporta las oportunidades ganadas del último año desde tu CRM.
  Columnas mínimas: cliente, sector, facturación, problema, solución, resultado medible.
- **servicios_pricing.csv** → tu catálogo de servicios. Si lo tienes en PDF o en la web,
  conviértelo a CSV o pídeselo a Claude en un paso previo.
- **plantilla_propuesta.md** → la última propuesta que enviaste, limpia de datos de cliente y
  convertida a markdown con las secciones estándar.

## Nota importante

Este prompt está pensado para **servicios de consultoría a PYMEs españolas** (1-50M€).
Si vendes productos físicos, SaaS, o servicios recurrentes, ajusta la plantilla
y la estructura del scope. El flujo (prospecto + casos + pricing → web espectacular + email)
es el mismo para cualquier venta B2B.

---

Creado por Isaac Romà · https://isaacroma.com
