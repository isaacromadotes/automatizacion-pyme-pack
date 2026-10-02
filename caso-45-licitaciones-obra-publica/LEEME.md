# CASO 45 — Licitaciones de obra pública

**Creado por Isaac Romà · https://isaacroma.com**

---

## El problema que resuelve

Si tu empresa depende de obra pública, cada licitación que no ves es dinero que pierdes. La mayoría de pymes constructoras se enteran de los concursos por casualidad: un comercial avisa, un conocido lo menciona, se publica tarde en un boletín.

Resultado: presentas 3 ofertas al mes cuando podrías presentar 12. Y las que presentas, muchas veces las ves tarde y preparas la propuesta con prisas.

Este sistema rastrea los portales de contratación pública, filtra las licitaciones por tu CNAE, zona geográfica, importe y tipo de obra, y genera cada semana un **informe visual** con las que de verdad encajan contigo.

---

## Qué contiene este ZIP

- `LEEME.md` — este archivo
- `prompt.txt` — el prompt que pegas en Claude Code
- `criterios_busqueda.csv` — tus criterios de filtrado (CNAE, zona, importe, tipo de obra)
- `licitaciones_ejemplo.csv` — simulación de 12 licitaciones publicadas en un mes

---

## Cómo usarlo paso a paso

1. **Instala Claude Code** siguiendo las instrucciones oficiales de Anthropic.
2. **Crea una carpeta** llamada `Ejemplo Claude Code` dentro de tu carpeta de Descargas.
3. **Copia los dos CSV** (`criterios_busqueda.csv` y `licitaciones_ejemplo.csv`) dentro de esa carpeta.
4. **Abre tu terminal** (iTerm en Mac, PowerShell en Windows) y escribe `claude` para arrancar Claude Code.
5. **Arrastra `LEEME.md` y `prompt.txt`** a la ventana de Claude Code — así entiende el contexto completo antes de ejecutar.
6. **Pega el contenido de `prompt.txt`** en el chat.
7. **Cambia las variables** `[EMPRESA]` y `[MES AÑO]` por tus datos reales.
8. **Pulsa Enter** y deja que Claude Code trabaje.

Claude Code generará tres cosas en la misma carpeta:
- Un **HTML visual** con las 5 licitaciones que más encajan contigo (ordenadas por plazo urgente).
- Un **Excel** con las 12 licitaciones del mes con filtros aplicados.
- Un **email semanal** listo para enviar al equipo comercial.

---

## De dónde sacar los datos reales en tu ERP

- **Plataforma de Contratación del Sector Público (PLACSP)**: descarga el XML/CSV diario desde contrataciondelestado.es
- **Boletines autonómicos**: DOGV (Generalitat Valenciana), BOCA (Andalucía), BOCM (Madrid), etc.
- **Diputaciones y ayuntamientos grandes**: cada uno con su perfil del contratante
- **Suscripciones privadas**: Insight View, Vortal, Licitia (de pago, agregadores)

Lo ideal es que un script automatizado descargue cada noche los nuevos pliegos y los guarde como CSV. Si no lo tienes montado todavía, podemos ayudarte a configurarlo.

---

## ⚠️ Nota importante

Este prompt está diseñado para **empresas de construcción y edificación** (CNAE 41-43) que operan con obra pública. Si tu empresa está en otro sector (suministros, servicios, consultoría al sector público), los criterios de filtrado del CSV cambian — pero la lógica del prompt es la misma.

Los datos del ZIP son ficticios. Simulan la actividad de una constructora de Levante especializada en edificación residencial y rehabilitación.

---

**Creado por Isaac Romà · https://isaacroma.com**
