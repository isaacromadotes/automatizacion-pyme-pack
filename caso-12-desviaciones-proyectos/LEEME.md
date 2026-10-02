# Caso 12 — Detecta proyectos que se están comiendo tu margen antes de que sea tarde

## El problema real

Diriges una consultora, una asesoría, un estudio de arquitectura o una empresa de servicios profesionales. Tus equipos imputan horas cada semana. A final de trimestre descubres que **tres proyectos han consumido el 130% del presupuesto de horas y solo llevan el 60% de avance**. El margen se ha evaporado. Nadie te avisó.

El problema no es la gente. Es que **el control de desviaciones está en la cabeza del jefe de proyecto**, no en un sistema. Cuando se detecta, ya es tarde para renegociar con el cliente o reasignar equipo.

Este pack te enseña a montar en 3 minutos un sistema de alerta temprana que te dice, con semáforo visual, qué proyectos se te están yendo de las manos **antes de que quemes el margen**.

## Qué contiene este ZIP

- `LEEME.md` — Este archivo.
- `prompt.txt` — El prompt que pegarás en Claude Code para generar el análisis completo.
- `proyectos.csv` — Datos ficticios de 8 proyectos (Consulting Horizonte S.L.). Cambia por los tuyos.
- `horas_imputadas.csv` — 160 imputaciones ficticias por persona, proyecto y fecha.
- `instrucciones_para_crear_tabla_excel.txt` — Guía de estilo corporativo para que el Excel salga profesional.

## Cómo usarlo — Paso a paso

1. **Instala Claude Code** siguiendo la guía oficial: https://docs.claude.com/claude-code
2. **Descomprime este ZIP** en una carpeta de tu ordenador. Ejemplo:
   `C:\Users\tuUsuario\Downloads\Caso 12 Desviaciones`
3. **Abre la terminal** (Windows Terminal, iTerm, CMD) y navega a esa carpeta:
   `cd "C:\Users\tuUsuario\Downloads\Caso 12 Desviaciones"`
4. **Lanza Claude Code**:
   `claude`
5. **Arrastra los 3 archivos** (LEEME.md, prompt.txt y los CSVs) sobre la ventana de Claude Code para que los tenga como contexto.
6. **Abre `prompt.txt`**, cámbiale las variables:
   - `[EMPRESA]` → nombre real de tu empresa
   - `[MES AÑO]` → periodo que quieres analizar (ej: "Septiembre 2026")
   - `@ruta/` → la ruta real donde descomprimiste (ej: `@C:\Users\tuUsuario\Downloads\Caso 12 Desviaciones\`)
7. **Copia todo el prompt**, pégalo en Claude Code y pulsa **Enter**.
8. En 2-3 minutos tendrás: el dashboard web abierto en tu navegador, el Excel con formato corporativo y el informe HTML de alertas en vertical 9:16.

## De dónde sacar los datos en tu ERP

Los dos CSVs que necesitas los saca cualquier ERP o gestor de proyectos moderno:

- **A3 ERP** — Módulo Proyectos → Informes → "Partes de horas" y "Cartera de proyectos". Exporta a CSV.
- **Sage 200 / Sage Despachos** — Análisis de rentabilidad de proyectos → Exportar a Excel → guardar como CSV.
- **Holded** — Proyectos → Vista tabla → botón Exportar. Para horas: módulo Team → Timesheet → Exportar.
- **SAP Business One** — Módulo Gestión de Proyectos → Consulta rápida → exportar. Horas: transacción CATS.
- **Odoo** — Aplicación Proyecto → Vista lista → Exportar. Horas: Timesheets → Exportar todo.
- **Notion o ClickUp** — Vista Database → menú "..." → Export as CSV.
- **Excel manual** — Si aún llevas las horas en un Excel, ya tienes el trabajo hecho: guarda cada hoja como CSV desde "Archivo → Guardar como".

**Mínimo imprescindible:**
- `proyectos.csv`: `proyecto_id`, `nombre`, `cliente`, `responsable`, `horas_presupuestadas`, `fecha_inicio`, `fecha_fin_prevista`, `presupuesto_eur`, `avance_estimado_pct`
- `horas_imputadas.csv`: `fecha`, `proyecto_id`, `persona`, `horas`, `tarifa_hora_eur`

## ⚠️ Nota importante

Este caso está diseñado para **empresas de servicios profesionales** (consultoría, asesoría, ingeniería, arquitectura, despachos legales, agencias). Si tu negocio es producto o retail, la lógica del análisis (horas vs avance) no aplica directamente — pero la estructura del prompt sirve como plantilla para adaptarla a tu caso (unidades producidas vs planificadas, ventas vs objetivo, etc.).

Los umbrales de alerta (10% / 15%) son estándar de la industria pero puedes cambiarlos en el bloque "CONTEXTO DE LA EMPRESA" del prompt según tu tolerancia al riesgo.

---

Creado por Isaac Romà · https://isaacroma.com
