# CASO 09 — Partes de obra digitales sin papel

## El problema real

En construcción, los partes de trabajo siguen en papel. El operario los rellena a medias en el tajo, se guardan arrugados en el bolsillo, llegan el viernes a oficina (si llegan) y alguien los pasa al Excel el lunes.

Resultado: no sabes cuántas horas llevas gastadas en cada obra hasta que ya te has comido el margen. La desviación la ves cuando ya no puedes hacer nada.

**Lo que se pierde con este sistema:**
- Horas mal imputadas (van a la obra que "se acuerda" el operario)
- Sobrecostes que aparecen 2-3 semanas tarde
- Discusiones con clientes por horas no justificadas
- Certificaciones que salen tarde y flujo de caja resentido

Este pack te muestra cómo Claude Code monta un sistema de partes digitales funcional en minutos, con panel de jefe de obra y alerta automática de sobrecoste.

---

## Qué contiene este ZIP

- `LEEME.md` — Este archivo
- `prompt.txt` — El prompt que pegarás en Claude Code
- `partes_semana.csv` — Partes de trabajo de una semana (36 registros, 3 obras)
- `presupuesto_mod.csv` — Presupuesto de mano de obra por obra y semana
- `obras_activas.csv` — Obras en curso (código, cliente, jefe de obra, presupuesto)

---

## Cómo usarlo paso a paso

### 1. Instala Claude Code
Si aún no lo tienes: https://docs.claude.com/claude-code
Necesitas una cuenta de Anthropic (plan Pro o superior recomendado).

### 2. Prepara la carpeta
Crea una carpeta en tu ordenador, por ejemplo:
- Windows: `C:\Users\tunombre\Downloads\Partes Obra\`
- Mac: `~/Downloads/Partes Obra/`

Descomprime este ZIP dentro de esa carpeta.

### 3. Abre Claude Code
Abre la terminal (Windows: PowerShell / Mac: Terminal) y escribe:
```
claude
```

### 4. Arrastra los archivos de contexto
Antes de pegar el prompt, arrastra a la terminal estos dos archivos:
- `LEEME.md` (para que Claude entienda el objetivo)
- `prompt.txt` (para que ejecute la metodología)

Así Claude tiene el contexto completo antes de arrancar.

### 5. Pega el prompt
Abre `prompt.txt`, copia todo su contenido y pégalo en Claude Code.

### 6. Cambia las variables
Antes de pulsar Enter, sustituye:
- `[EMPRESA]` → nombre de tu constructora
- `[SEMANA AÑO]` → ej. "Semana 37 2026"
- Las rutas `@ruta/` → la ruta real donde tienes los CSVs

### 7. Enter y espera
Claude Code te genera:
- Formulario móvil para que el operario fiche horas
- Panel del jefe de obra con horas por obra vs presupuesto
- Alerta roja automática si la obra supera el 110% presupuestado
- PDF resumen semanal para dirección

---

## De dónde sacar los datos reales en tu ERP

Cuando quieras hacerlo con datos de tu empresa, exporta a CSV desde:

- **A3ERP / A3CON** → Módulo Obras > Partes de trabajo > Exportar Excel
- **Sage 50 / Sage 200 Construcción** → Producción > Partes > Listados > Exportar
- **Presto** → Diagrama > Certificaciones > Tabla de partes
- **Menfis** → Partes de trabajo > Consulta > Exportar CSV
- **PrimaverA (obra)** → Recursos humanos > Horas trabajadas > Exportar
- **SAP (módulo PS)** → CJ74 (horas confirmadas por proyecto) > Exportar a CSV
- **Odoo (módulo Project + Timesheets)** → Partes de horas > Filtrar > Descargar
- **Holded** → Proyectos > Tiempos > Exportar

Si no tienes ERP y trabajas con Excel, exporta la hoja como CSV (Guardar como > CSV UTF-8).

---

## Nota importante — sector construcción

Este prompt está diseñado específicamente para **empresas constructoras y promotoras españolas** (obra civil, edificación, reformas). Contempla:

- Categorías profesionales del Convenio General de la Construcción
- Estructura obra > tajo > partida
- Presupuesto de mano de obra (MOD) semanal
- Umbral de alerta del 110% (estándar en control de producción)

Si tu sector es distinto (industria, servicios), el prompt sigue funcionando pero cambia las etiquetas de "obra" por "proyecto" o "centro de coste" al pegar el prompt.

---

## Firma

Creado por **Isaac Romà** · https://isaacroma.com

Economista, 20 años como CEO/CFO/COO en PYMEs industriales españolas.
Metodología de automatización ejecutiva para empresas de 1 a 50M€.

→ Reunión gratuita de 30 min: https://calendly.com/asesor-online-ia/30min
