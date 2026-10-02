# Caso 18 · Cuadro de mando con flujo de aprobación — Delegar sin perder el control

> Gerente de PYME de servicios: pasa de **60-70 h/semana aprobando todo** a ver el estado del negocio en **10 segundos** y aprobar solo lo que supera el umbral del equipo.

## 🎯 Problema que resuelve

En una PYME de servicios profesionales de 8-25 personas, el gerente acaba atrapado en el mismo bucle: aprueba cada compra, revisa cada propuesta comercial, firma cada contratación, valida cada gasto. No es que no quiera delegar, es que sin datos delegar es un acto de fe: si no lo ve él, no se fía, porque no tiene visibilidad real de lo que pasa en cada área. Resultado: 60-70 horas semanales, cero tiempo para estrategia, equipo bloqueado esperando el OK del jefe y clientes que perciben que todo depende de una persona (lo cual, por cierto, también destruye valoración si algún día quiere vender la empresa). El problema no se resuelve con un curso de delegación ni con "confiar más": se resuelve con dos cosas concretas que este pack entrega juntas. Primero, un cuadro de mando por área con semáforos verde/ámbar/rojo sobre los KPIs reales de Comercial, Proyectos, Finanzas y RRHH, de modo que en 10 segundos el gerente ve dónde hay desviación sin preguntar a nadie. Segundo, un panel de aprobaciones con flujo escalonado por importe y responsable, que define por escrito quién puede aprobar qué hasta cuánto, y hace llegar al gerente únicamente lo que supera el umbral del nivel inferior. Visibilidad + reglas claras = delegación con red.

## 📦 Archivos del pack

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Documento inicial con la explicación del caso. |
| `prompt.txt` | Prompt listo para pegar en Claude Code. |
| `kpis_areas.csv` | 16 KPIs de 4 áreas (Comercial, Proyectos, Finanzas, RRHH) con objetivo, real y estado semáforo. |
| `aprobaciones_pendientes.csv` | 12 aprobaciones pendientes de ejemplo (compras, contrataciones, propuestas, gastos). |
| `equipo.csv` | 12 personas del equipo con puesto, área y nivel de aprobación en €. |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la [documentación oficial](https://docs.anthropic.com/en/docs/claude-code): `npm install -g @anthropic-ai/claude-code`
2. **Descomprime este pack** en una carpeta local (ej. `C:\Delegacion\`) y abre la terminal dentro con el comando `claude`.
3. **Arrastra a la ventana de Claude Code** el `LEEME.md`, el `prompt.txt` y los 3 CSV para que tenga todo el contexto.
4. **Copia el contenido de `prompt.txt`**, pégalo en Claude Code y sustituye `[EMPRESA]`, `[MES AÑO]` y `[RUTA]` por tus datos reales.
5. **Pulsa Enter**: Claude Code genera el cuadro de mando web con semáforos por área y el PDF con los flujos de aprobación por nivel y responsable.

## 🔌 Cómo exportar los datos desde tu ERP

| Dato | A3ERP / A3CON | Sage 50/200 | Holded | SAP Business One | Odoo | Contasol / ContaPlus |
|---|---|---|---|---|---|---|
| KPIs comerciales (facturación, propuestas, conversión) | Módulo Comercial → Estadísticas → Exportar | Ventas → Informes → Exportar | Ventas → Informes → Exportar | Ventas → Informes → Exportar | CRM / Ventas → Informes → Exportar | Ventas → Listado → Exportar |
| KPIs proyectos (plazo, horas facturables, desviación) | Proyectos → Partes y rentabilidad → Exportar | Proyectos → Rentabilidad → Exportar | Proyectos → Rentabilidad → Exportar | Project Management → Exportar | Proyectos / Hojas de horas → Exportar | — (gestión externa) |
| KPIs finanzas (cobro medio, EBITDA, tesorería) | Financiero → Cuadro de mando → Exportar | Financiero → Analítica → Exportar | Finanzas → Informes → Exportar | Financials → Informes → Exportar | Contabilidad → Informes → Exportar | Mayor y balances → Exportar |
| KPIs RRHH (rotación, absentismo, formación) | A3NOM → Estadísticas → Exportar | Sage Nóminas → Informes → Exportar | Factorial / Sesame / Bizneo → Exportar | HR → Informes → Exportar | Empleados → Informes → Exportar | Nóminas → Listado → Exportar |

> ⚠️ **Nota de sector:** este pack está diseñado para **empresas de servicios profesionales de 8-25 personas** (consultoría, asesoría, ingeniería, arquitectura, agencias, despachos) con estructura gerente + responsables de área. Si tu empresa es industrial, comercial o logística, cambia los nombres de las 4 áreas y los KPIs por los tuyos (Producción, Almacén, Ventas, Administración); el flujo y la lógica de aprobación se mantienen. Para completar el control de gestión, combina con el [caso-01 (cierre mensual)](../caso-01-cierre-mensual/) y el [caso-06 (rentabilidad por cliente)](../caso-06-rentabilidad-clientes/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años en C-Suite.
Ayudo a **PYMEs industriales, mayoristas y de construcción (1-50M€)** a automatizar operaciones y recuperar margen con IA aplicada al negocio real, no a la tecnología.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **Automatización a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min conmigo:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>cuadro de mando pyme servicios profesionales, flujo de aprobación por nivel, delegar sin perder control gerente, dashboard semáforo kpis áreas, panel aprobaciones compras pyme, matriz de firmas y gastos, delegación control pyme 8-25 personas, kpis comercial proyectos finanzas rrhh, gerente atrapado operativa delegar, política de aprobaciones pyme</sub>
