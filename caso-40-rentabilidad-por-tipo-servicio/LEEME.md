# Caso 40 — Rentabilidad real por tipo de servicio

## El problema

En asesorías y despachos profesionales (contable, fiscal, laboral, legal) se cobra una cuota mensual por cliente y servicio, pero **nadie mide cuántas horas reales consume cada servicio**.

Resultado: hay servicios que facturan bien pero cuestan más horas que lo que ingresan. Normalmente el laboral: muchas incidencias, nóminas, altas y bajas, reclamaciones TGSS… por 180€/mes.

**Si no cruzas horas × coste/hora contra honorarios, estás regalando dinero sin saberlo.**

## Qué contiene este ZIP

- `LEEME.md` — este archivo
- `prompt.txt` — el prompt que pegarás en Claude Code
- `horas_servicio.csv` — horas reales trabajadas por gestor, cliente, servicio y mes
- `honorarios_servicio.csv` — cuota mensual que cobras a cada cliente por cada servicio
- `costes_gestor.csv` — coste por hora de cada gestor (salario bruto + SS / horas productivas)

## Cómo usarlo paso a paso

1. **Instala Claude Code** (si no lo tienes): https://claude.com/claude-code
2. **Crea una carpeta** en tu ordenador y copia dentro los 3 CSVs y este LEEME.md
3. **Abre la terminal** en esa carpeta y escribe: `claude`
4. **Arrastra el LEEME.md y el prompt.txt** a la ventana de Claude Code para que entienda el contexto
5. **Pega el prompt** y cambia estas variables:
   - `[EMPRESA]` → nombre de tu asesoría
   - `[MES AÑO]` → periodo analizado (ej: "enero-junio 2026")
   - `@ruta/` → ruta donde están tus CSVs
6. **Pulsa Enter** y espera. Claude Code generará el Excel con ranking + gráfico y un HTML con las propuestas.

## De dónde sacar los datos reales en tu ERP

- **A3 Asesor / A3 ERP (Wolters Kluwer)**: módulo "Control de tiempos" → exportar horas por profesional/cliente/servicio. Honorarios → "Facturación de servicios recurrentes".
- **Sage Despachos Connected**: "Partes de trabajo" para horas, "Contratos de servicios" para honorarios.
- **Holded**: Proyectos → Timetracking (horas); Facturación recurrente (cuotas).
- **Odoo**: módulo Timesheets (horas), Subscriptions (cuotas mensuales).
- **Clockify / Toggl + hoja Excel**: si no tienes ERP integrado, exporta las horas del tracker y crúzalo con tu listado de clientes.

**Coste/hora del gestor**: (Salario bruto anual + Seguridad Social empresa) ÷ (Horas productivas anuales ≈ 1.600h).

## Nota importante — Sector

Este prompt está diseñado para **asesorías y despachos profesionales** (contable, fiscal, laboral, legal, auditoría, consultoría). Los servicios tipo (contabilidad, fiscal, laboral, asesoramiento) son los habituales del sector.

Si tu negocio es otro servicio profesional (arquitectura, ingeniería, agencia marketing, abogacía…), funciona igual: solo cambia los nombres de los servicios en tus CSVs y Claude Code se adaptará.

---

Creado por Isaac Romà · https://isaacroma.com
