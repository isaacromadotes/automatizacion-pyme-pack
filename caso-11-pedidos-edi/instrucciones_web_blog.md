# Bloque para la web/blog de descarga del caso 11

## Cómo usar este pack

Descarga el ZIP y descomprímelo en tu ordenador. Dentro encontrarás dos ficheros que dan contexto a la IA (`LEEME.md` y `prompt.txt`) más una carpeta `csv/` con los datos de ejemplo.

**El paso clave que la mayoría olvida:** antes de pegar el prompt, **arrastra el LEEME.md y el prompt.txt a la ventana de Claude Code**. Así la IA lee primero todo el contexto (el problema que resuelves, dónde están los datos, qué formato tienen) y luego ejecuta el prompt con esa información en la cabeza. Sin ese paso, la IA trabaja a ciegas y el resultado es peor.

El flujo correcto es:

1. Abre la carpeta descomprimida en tu terminal
2. Escribe `claude` y pulsa Enter
3. Arrastra **LEEME.md** a la ventana de Claude Code
4. Arrastra **prompt.txt** a la ventana de Claude Code
5. Abre `prompt.txt` en un editor de texto, cambia `[EMPRESA]` y `[MES AÑO]` si quieres personalizar
6. Copia el contenido del prompt y pégalo en Claude Code
7. Pulsa Enter y déjalo trabajar

Cuando termine, te abrirá una web local con la simulación completa del flujo EDI → pedido → albarán. Puedes descargar el PDF del albarán directamente desde ahí.

Si quieres probarlo con tus pedidos reales, sustituye los CSVs de la carpeta `csv/` por los tuyos manteniendo los nombres de las columnas. El prompt no cambia.
