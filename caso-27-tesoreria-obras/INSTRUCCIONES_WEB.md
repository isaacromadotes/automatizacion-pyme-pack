# Bloque para la web / blog de isaacroma.com

## Cómo usar este pack

Este ZIP contiene todo lo necesario para separar la tesorería por obra de tu constructora en menos de 5 minutos, incluso si nunca has usado Claude Code.

**Pasos**:

1. **Descomprime el ZIP** en una carpeta de tu equipo.
2. **Abre Claude Code** (si no lo tienes instalado, sigue la guía en https://isaacroma.com/blog).
3. **Arrastra a la ventana de Claude Code**, en este orden, estos archivos:
   - `LEEME.md` (para que entienda el contexto del caso)
   - `prompt.txt` (las instrucciones exactas que debe ejecutar)
   - Los 3 archivos CSV (`cobros_obra.csv`, `pagos_obra.csv`, `certificaciones_pendientes.csv`)

   Al arrastrarlos, Claude Code los lee automáticamente y tiene todo el contexto antes de empezar.

4. **Copia el contenido de `prompt.txt`** y pégalo en la terminal.
5. **Cambia las 3 variables** entre corchetes al principio del prompt:
   - `[EMPRESA]` → el nombre de tu constructora
   - `[MES AÑO]` → el periodo que analizas
   - `[RUTA]` → la carpeta donde están los CSVs
6. **Pulsa Enter**. En 2-3 minutos tendrás:
   - Un panel web con la posición de caja de cada obra
   - Un informe HTML ejecutivo listo para presentar a dirección o al banco
   - Las alertas automáticas de qué obra está financiando a cuál

**Si quieres hacerlo con los datos reales de tu empresa**, reserva una reunión gratuita de 30 minutos en https://calendly.com/asesor-online-ia/30min y te ayudo a conectar tu ERP.
