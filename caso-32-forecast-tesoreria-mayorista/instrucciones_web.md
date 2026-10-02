# Instrucciones de uso — copiar/pegar en la landing o blog

## Cómo usar este pack con Claude Code

Este ZIP contiene un prompt profesional + datos de ejemplo para que Claude Code genere un **forecast diario de tesorería a 90 días** con una web interactiva y un PDF ejecutivo.

### Pasos:

1. **Descomprime el ZIP** en una carpeta de tu PC (recomendado: `~/Descargas/Ejemplo Claude Code/`).

2. **Abre tu terminal** en esa carpeta y arranca Claude Code con el comando `claude`.

3. **Arrastra DOS archivos** a la ventana de Claude Code:
   - `LEEME.md` → para que entienda el contexto, el problema y de dónde salen los datos.
   - `prompt.txt` → la instrucción exacta que debe ejecutar.

4. **Pega el contenido del `prompt.txt`** y pulsa Enter.

5. Claude Code leerá los CSVs, calculará el forecast, montará una web local y la abrirá en tu navegador. También generará un PDF ejecutivo.

> **Importante:** arrastrar el LEEME.md antes del prompt es lo que marca la diferencia. Le da a Claude Code el contexto completo (sector, problema, caso de uso) antes de ejecutar, y los entregables salen mucho más alineados con lo que necesitas.

### Para usarlo con tus propios datos

Sustituye los 3 CSVs por los exports de tu ERP (A3, Sage, Holded, SAP, Odoo…). Las instrucciones de dónde sacar cada informe están dentro del `LEEME.md`.
