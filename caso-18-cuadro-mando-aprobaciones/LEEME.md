# Cuadro de Mando con Flujo de Aprobación — Delegar sin perder el control

## El problema que resuelve

Eres gerente de una PYME de servicios y estás en todo. Apruebas cada compra, revisas cada propuesta, decides cada contratación. No porque quieras — porque si no lo ves tú, no te fías.

Resultado: 60-70 horas semanales, cero estrategia, equipo bloqueado esperando tu OK, y clientes que ven que todo pasa por una persona.

El motivo real no es que no quieras delegar. Es que **no tienes visibilidad** de lo que ocurre si sueltas el control. Sin datos, delegar es un acto de fe.

Este pack resuelve exactamente eso: un **cuadro de mando por área con semáforos** y un **panel de aprobaciones con flujos según nivel de cada responsable**. Ves lo que pasa en 10 segundos, y solo aprueba el gerente lo que supera el umbral de su equipo.

## Qué contiene este ZIP

- `LEEME.md` — este archivo
- `prompt.txt` — el prompt que pegarás en Claude Code
- `kpis_areas.csv` — 16 KPIs de las 4 áreas (Comercial, Proyectos, Finanzas, RRHH) con objetivo, real y estado semáforo
- `aprobaciones_pendientes.csv` — 12 aprobaciones pendientes de ejemplo (compras, contrataciones, propuestas, gastos)
- `equipo.csv` — 12 personas del equipo con puesto, área y nivel de aprobación en €

## Cómo usarlo paso a paso

1. **Instala Claude Code** en tu equipo si aún no lo tienes: https://claude.ai/code
2. **Descomprime este ZIP** en una carpeta (por ejemplo `C:\Users\tu_usuario\Downloads\Delegacion\`)
3. **Abre la terminal** (iTerm en Mac, Windows Terminal en PC) y escribe `claude`
4. **Arrastra a la terminal** los archivos `LEEME.md`, `prompt.txt` y los 3 CSVs para que Claude tenga contexto completo
5. **Copia el contenido de `prompt.txt`** y pégalo
6. **Sustituye las variables** entre corchetes (`[EMPRESA]`, `[MES AÑO]`, `[RUTA]`) por tus datos reales
7. **Pulsa Enter** y Claude Code generará el cuadro de mando web + el PDF con los flujos de aprobación

## De dónde sacar tus datos en el ERP

- **KPIs comerciales** (facturación, propuestas, conversión) → CRM (HubSpot, Pipedrive, Salesforce) o módulo comercial de tu ERP (Sage 200, A3ERP, Holded, Odoo)
- **KPIs proyectos** (plazo, horas facturables, desviación) → herramienta de gestión (Jira, Asana, ClickUp) o Sage Proyectos, A3ERP Proyectos
- **KPIs finanzas** (cobro medio, EBITDA, tesorería) → módulo financiero (Sage 50/200, A3CON, Contasol, Holded, SAP Business One)
- **KPIs RRHH** (rotación, absentismo, formación) → software de nóminas (A3NOM, Sage Nóminas) o gestor de RRHH (Factorial, Sesame, Bizneo)
- **Aprobaciones y equipo** → tu directorio interno + política actual de firmas y compras

Exporta cada bloque a CSV con la misma estructura que los archivos de ejemplo y pégalos en la carpeta antes de ejecutar el prompt.

## Nota importante sobre el sector

Este prompt está diseñado para **empresas de servicios profesionales** (consultoría, asesoría, ingeniería, arquitectura, agencias, despachos) de **8-25 personas** con estructura de gerente + responsables de área. Si tu empresa es industrial, comercial o logística, cambia los nombres de las 4 áreas y los KPIs por los tuyos (por ejemplo Producción, Almacén, Ventas, Administración) — el flujo y la lógica de aprobación se mantienen igual.

---

Creado por Isaac Romà · https://isaacroma.com
