# Caso 46 — Equipo saturado: libera 20h/semana sin contratar

## El problema

Tu asesoría (o despacho profesional) no puede captar más clientes porque el equipo está al 100%. Pero cuando miras de verdad en qué se va el tiempo, descubres que el **60% son tareas de bajo valor**: entrada de datos, conciliaciones manuales, recordatorios de cobro, generación de facturas recurrentes, archivo de documentos…

El dolor real: el socio quiere crecer, pero contratar sale caro, forma al nuevo lleva meses, y mientras tanto rechaza clientes nuevos o los atiende mal.

Este prompt detecta en minutos qué tareas se pueden automatizar, cuántas horas liberas y cuánta capacidad extra te da el equipo que ya tienes.

## Qué contiene este ZIP

- **LEEME.md** — este archivo
- **prompt.txt** — el prompt que vas a pegar en Claude Code
- **tareas_equipo.csv** — ejemplo con 19 tareas típicas de una asesoría
- **costes_equipo.csv** — ejemplo con 6 personas y su coste/hora
- **instrucciones_html.txt** — guía de diseño para la web visual
- **instrucciones_excel.txt** — guía de diseño para el Excel

## Cómo usarlo (5 minutos)

1. **Instala Claude Code** si no lo tienes: https://claude.com/claude-code
2. **Descomprime este ZIP** en una carpeta tuya (ej: `D:\caso_46\`)
3. **Abre la terminal** en esa carpeta y escribe: `claude`
4. **Copia los CSVs** por tus datos reales (manteniendo las columnas) o prueba primero con los de ejemplo
5. **Abre el prompt.txt**, cambia `[EMPRESA]` y `[MES AÑO]` por los tuyos
6. **Pégalo en Claude Code** y pulsa Enter

En 1-2 minutos tienes la web visual, el Excel y el plan de automatización en HTML.

## De dónde sacar tus datos reales

### Columna `tareas` (listado de qué hace tu equipo)
- **A3 Asesor / A3 ERP**: módulo "Gestión de tareas" o "Workflow"
- **Sage Despachos Profesionales**: menú Tareas → Listado
- **Holded**: Proyectos → Tareas → exportar
- **Odoo**: módulo Proyecto → vista lista → exportar CSV
- **Sin ERP**: pide al equipo que apunte 1 semana lo que hacen (Toggl, hoja Excel compartida)

### Columna `horas_semanales`
- Herramientas de control horario: Toggl, Clockify, Factorial, Sesame
- Si no tienes: estima con el responsable de cada tarea (sincero > exacto)

### Columna `coste_hora` (archivo costes_equipo.csv)
- Nómina bruta anual + SS a cargo de empresa ÷ 1.600 horas efectivas/año
- O usa el salario bruto mensual × 14 ÷ 1.600 como aproximación rápida

## Importante

Este prompt está **diseñado para servicios profesionales** (asesorías, despachos de abogados, consultoras, agencias). Si tu empresa es industrial o retail, los tipos de tareas serán distintos — el prompt sigue funcionando pero adapta las categorías en `tareas_equipo.csv`.

---

Creado por Isaac Romà · https://isaacroma.com
