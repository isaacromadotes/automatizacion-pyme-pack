# Bloque para la web / blog (planillasexcel.es o isaacroma.com)

## Cómo usar este pack con Claude Code

Este ZIP contiene todo lo necesario para que Claude Code analice las ventas de tu equipo comercial y genere, en un solo paso, un dashboard Excel y una presentación web ejecutiva.

**Sigue estos pasos:**

1. Descomprime el ZIP en una carpeta local. Sugerido: `C:\Users\[tu usuario]\Downloads\Ejemplo Claude Code\Vídeo 26\`
2. Abre la terminal (iTerm en Mac, Terminal en Windows) dentro de esa carpeta.
3. Escribe `claude` y pulsa Enter.
4. **Arrastra los dos archivos siguientes a la ventana de Claude Code antes de pegar nada:**
   - `LEEME.md`
   - `prompt.txt`

   Esto hace que Claude Code entienda el contexto completo (quién eres, qué resuelve el prompt, cómo están estructurados los CSVs) antes de ejecutar la petición.

5. Después de arrastrar, pega el contenido de `prompt.txt` como mensaje y pulsa Enter.
6. Claude Code generará el Excel y la presentación web. Cuando termine, se abrirá en tu navegador.

**Si tienes datos reales:**
Sustituye `ventas_detalle.csv` y `objetivos.csv` por los exports de tu ERP (A3, Sage, Holded, SAP, Odoo…) manteniendo los nombres de archivo y las columnas que indica el `LEEME.md`.
