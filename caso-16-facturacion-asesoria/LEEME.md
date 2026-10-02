# Caso 16 · Facturación masiva de una asesoría en minutos

## El problema

Una gestoría con 400 clientes tarda 2 días completos a fin de mes en facturar a sus propios clientes. Un socio o un administrativo calcula honorarios, genera facturas una a una, prepara la remesa para el banco y envía los emails. Es el mes que no se factura porque se está facturando.

Este caso reduce ese trabajo a **minutos** con un solo prompt de Claude Code.

## Qué contiene este ZIP

- **LEEME.md** — Este archivo.
- **prompt.txt** — El prompt listo para pegar en Claude Code.
- **clientes.csv** — 400 clientes ficticios de "Asesoría Martínez y Asociados" con NIF, IBAN, email, cuota mensual, extras y forma de pago. Total facturación: 127.840€.

Cuando ejecutes el prompt, Claude Code generará:
- 3 facturas HTML de ejemplo optimizadas para pantalla 9:16 (1080x1920)
- 3 emails HTML de ejemplo optimizados para 9:16
- La remesa SEPA en XML (norma 19.14, esquema pain.008.001.02) lista para subir al banco
- Un Excel resumen con totales, detalle por cliente e incidencias

## Cómo usarlo (paso a paso)

1. Instala Claude Code si aún no lo tienes: https://claude.com/claude-code
2. Descarga y descomprime este ZIP en `C:\Users\isaac\Downloads\Ejemplo Claude Code\Vídeo 16\`
3. Abre la terminal en esa carpeta y ejecuta `claude`
4. Arrastra `LEEME.md`, `prompt.txt` y `clientes.csv` a la ventana de Claude Code (para que tenga el contexto completo)
5. Pega el contenido de `prompt.txt`
6. Cambia las variables `[EMPRESA]` y `[MES AÑO]` por tus datos reales (o déjalos con los valores por defecto para probar)
7. Pulsa Enter y espera

## De dónde sacar los datos reales de tu ERP

El CSV de ejemplo replica la estructura típica de un maestro de clientes. Estos son los caminos habituales según tu software:

- **A3ASESOR (Wolters Kluwer)** → Módulo Facturación → Maestros → Clientes → Exportar a Excel
- **Sage 50 / Sage Despachos** → Ficheros → Clientes → Utilidades → Exportar
- **Holded** → Contactos → Filtro "clientes" → Exportar CSV
- **Odoo** → Contactos → Filtros: Cliente → Acción → Exportar
- **SAP Business One** → Business Partners → Query Manager con campos CardCode, LicTradNum, IBAN, MailAddress

Después añade dos columnas manuales o desde tu hoja de honorarios: `cuota_mensual` y `extras_importe`.

## Nota importante

Este prompt está diseñado para **gestorías, asesorías y despachos profesionales españoles** que facturan cuotas mensuales recurrentes + servicios extras a sus clientes. Si tu modelo es distinto (facturación por horas, proyectos, productos), el prompt necesita ajustes en el paso 2 (cálculo) y en el layout de la factura.

La remesa SEPA generada sigue la norma 19.14 (pain.008.001.02) usada por bancos españoles para adeudos directos. Verifica con tu banco el esquema exacto (CORE vs B2B) antes de subir en producción.

---

Creado por Isaac Romà · https://isaacroma.com
