# INSTRUCCIONES PARA PUBLICAR EN LA WEB / BLOG

## Bloque corto para la página de descarga del pack

---

### Cómo usar este pack en Claude Code

1. **Descomprime el ZIP** en una carpeta de tu equipo (ej: `C:\Analisis\Erosion_Margen\`).
2. **Abre tu terminal** y navega a esa carpeta:
   ```
   cd C:\Analisis\Erosion_Margen
   ```
3. **Arranca Claude Code** escribiendo `claude` y pulsando Enter.
4. **Arrastra a la ventana de Claude Code los dos archivos siguientes**:
   - `LEEME.md`
   - `prompt.txt`

   Esto es importante: Claude leerá primero el contexto completo (el problema, los archivos del pack, cómo interpretar los datos) antes de ejecutar el prompt. Sin este paso, la IA ejecuta "a ciegas" y el resultado pierde precisión.

5. **Pega el contenido de `prompt.txt`** en el chat.
6. **Antes de pulsar Enter**, sustituye las variables entre corchetes:
   - `[EMPRESA]` → nombre de tu empresa.
   - `[MES AÑO]` → el periodo que quieras analizar.
7. **Pulsa Enter.** Claude Code validará los datos, calculará la erosión por causa, generará el dashboard HTML y lo abrirá automáticamente en tu navegador. Adicionalmente te dejará el informe en PDF.

### ¿Problemas al ejecutarlo?

- Si Claude Code no encuentra los CSVs, asegúrate de haber arrancado el programa **desde la carpeta** donde descomprimiste el ZIP.
- Si quieres usarlo con tus datos reales, basta con que sustituyas los CSVs del pack por los tuyos (manteniendo los nombres de columna). El prompt se adapta solo.

### Siguiente paso

Si quieres aplicarlo con los datos reales de tu empresa conectado a tu ERP, agenda una **llamada gratuita de 30 minutos** y te enseño cómo montarlo en una sesión:
👉 https://calendly.com/asesor-online-ia/30min

---

## Metadata para el post

- **Título sugerido**: "Descarga: Descompón la erosión del margen de tu mayorista en 5 minutos"
- **Meta descripción**: "Pack gratuito con prompt para Claude Code, CSVs de ejemplo y guía paso a paso. Averigua por qué pierdes margen cada año."
- **Categoría**: Casos resueltos · Mayorista
- **Tags**: margen bruto, análisis financiero, Claude Code, PYME, mayorista, distribución, CFO, automatización ejecutiva
- **CTA final**: Reunión gratuita 30 min
- **Imagen destacada**: `portada_v44_margen.png`
