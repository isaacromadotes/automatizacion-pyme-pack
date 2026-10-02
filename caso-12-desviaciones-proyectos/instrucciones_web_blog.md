# Bloque para la web / blog

Copia este bloque en la página del vídeo o en el post del blog donde se descarga el ZIP:

---

## Cómo usar este pack en Claude Code

1. **Descarga y descomprime** el ZIP en una carpeta de tu ordenador.
2. **Abre Claude Code** en esa misma carpeta (`cd` a la carpeta y luego `claude`).
3. **Arrastra a la ventana de Claude Code los tres archivos siguientes**:
   - `LEEME.md`
   - `prompt.txt`
   - `instrucciones_para_crear_tabla_excel.txt`

   Al hacerlo, Claude tendrá el contexto completo del caso, la guía de estilo del Excel y las instrucciones de negocio antes de ejecutar nada. **Sin este paso, el resultado será mucho más pobre.**

4. **Añade también los dos CSVs** (`proyectos.csv` y `horas_imputadas.csv`) o los tuyos propios.
5. **Abre `prompt.txt`**, sustituye `[EMPRESA]`, `[MES AÑO]` y `@ruta/` por tus valores reales, cópialo entero y pégalo en Claude Code.
6. **Pulsa Enter** y en 2-3 minutos tendrás el dashboard web, el Excel corporativo y el informe HTML de alertas.

> 💡 **Truco pro:** Si sustituyes los CSVs de ejemplo por los exportados de tu ERP (A3, Sage, Holded, SAP, Odoo…), el mismo prompt te generará el análisis con tus datos reales. Ese es el punto donde esto deja de ser un ejemplo y se convierte en tu sistema de control.

---
