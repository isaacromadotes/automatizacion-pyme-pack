# Caso 51 — Delegar sin perder el control

## El problema que resuelve

Eres gerente de una constructora. Estás en todo: cada compra, cada presupuesto, cada incidencia en obra pasa por ti. No porque quieras controlarlo, sino porque si no lo ves tú, se pierde dinero.

Resultado: 60-70 horas semanales, nunca creces, y cuando te vas de vacaciones la empresa se para.

Este pack monta en minutos el sistema que te deja **solo ver las excepciones**: un panel por obra con semáforos, un flujo de aprobación escalonado por importe, y un informe semanal de una sola página con lo que requiere tu decisión.

Recuperas 15-20 horas semanales. Delegas con datos, no con fe.

---

## Qué contiene el ZIP

- **LEEME.md** — este archivo
- **prompt.txt** — el prompt que pegarás en Claude Code
- **kpis_obra.csv** — datos ficticios de 4 obras con 6 KPIs cada una (avance, desviación coste, caja, incidencias, retrasos, margen)
- **aprobaciones.csv** — 10 solicitudes de compra/subcontrata/imprevisto pendientes, con importe y nivel al que escalan

Los dos CSV cruzan: cada aprobación referencia una obra del archivo de KPIs.

---

## Cómo usarlo paso a paso

1. **Instala Claude Code** si no lo tienes: https://docs.claude.com/claude-code
2. **Crea una carpeta** en tu equipo y mete dentro los 2 CSV, el LEEME.md y el prompt.txt
3. **Abre terminal** en esa carpeta y escribe `claude`
4. **Arrastra** el LEEME.md y el prompt.txt a la ventana de Claude Code para que entienda el contexto completo
5. **Abre el prompt.txt**, cambia las variables entre corchetes `[EMPRESA]`, `[MES AÑO]`, `[RUTA]` por los tuyos
6. **Pega el prompt** en Claude Code y pulsa Enter
7. Claude Code generará: dashboard Excel por obra + dashboard HTML consolidado + HTML con el flujo de aprobación + HTML del informe semanal. Levantará el servidor local para que lo veas en el navegador.

---

## De dónde sacar tus datos reales

Para `kpis_obra.csv` necesitas los KPIs de cada obra activa. Según tu ERP:

- **Presto / CYPE / Menfis** → Informes de certificación, control de coste y caja por obra
- **A3 Innuva / Sage 50c Construcción** → Módulo de obras: avance, desviación presupuestaria, caja
- **Holded / Odoo** → Proyectos → informe de rentabilidad por proyecto
- **SAP Business One** → Project Management module, consulta de proyectos activos
- **Excel manual** → Si llevas las obras en hojas separadas, exporta a CSV cada mes

Para `aprobaciones.csv` necesitas las solicitudes abiertas:

- Email / WhatsApp del jefe de obra pidiendo compra → vuélcalas en un CSV semanal
- Si usas una herramienta tipo **Procore, Autodesk Construction Cloud, Jotform** → export directo
- Si todo pasa por tu email → una tarde de volcado inicial y luego vas añadiendo

---

## ⚠️ Nota importante

Este prompt está diseñado para **constructoras y promotoras inmobiliarias españolas**. Los umbrales de aprobación (<1K€ jefe de obra / 1-5K€ dir. producción / >5K€ gerente) y los KPIs están pensados para empresas de 1-50M€ de facturación.

Si tu empresa es de otro sector (industria, servicios, distribución), el prompt funciona igual pero deberás ajustar los nombres de KPI y los tramos de importe a tu realidad.

---

Creado por Isaac Romà · https://isaacroma.com
