## Cómo usar este pack en Claude Code

Dentro del ZIP tienes 6 archivos: `LEEME.md`, `prompt.txt` y 4 CSV de ejemplo.

**El paso que casi nadie da** y que marca la diferencia entre un resultado mediocre y uno brutal:

Antes de pegar el prompt, **arrastra `LEEME.md` y `prompt.txt` dentro de la ventana de Claude Code** junto con tus CSV. Así la IA lee el contexto completo del caso — el problema, el modelo de negocio, los pesos del scoring, el formato esperado — antes de ejecutar nada. Sin ese contexto, Claude Code adivina. Con él, resuelve.

Flujo correcto:

1. Descomprime el ZIP en una carpeta.
2. Abre Claude Code en esa carpeta (`claude` en terminal).
3. Arrastra `LEEME.md` + `prompt.txt` + tus 4 CSV a la ventana.
4. Abre `prompt.txt`, cambia `[EMPRESA]`, `[MES AÑO]` y `@ruta/` por tus valores.
5. Pega el prompt. Enter.

En 2-3 minutos tendrás el dashboard HTML abierto en tu navegador y el PDF ejecutivo listo en la carpeta.
