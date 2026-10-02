# Caso 28 — Rentabilidad real por cliente en asesoría

## El problema que resuelve

Tu asesoría tiene cientos de clientes. Pagan una cuota mensual fija. Pero **nadie sabe cuánto cuesta de verdad atender a cada uno**.

Entre consultas telefónicas que no se facturan, rectificaciones de IVA, dudas por WhatsApp y expedientes complejos, hay clientes que te hacen perder dinero cada mes. Y no lo detectas porque todos pagan "lo mismo".

Este caso te permite cruzar en 30 segundos:
- Horas reales dedicadas por cliente
- Honorarios que cobras
- Coste real por hora de cada gestor

Y descubrir qué porcentaje de tu cartera tiene **margen negativo**, con un plan de acción concreto por cliente: subir precio, limitar scope o reestructurar.

---

## Qué contiene este ZIP

- `LEEME.md` → este archivo
- `prompt.txt` → el prompt que pegarás en Claude Code
- `horas_cliente.csv` → ejemplo de horas por cliente/gestor (20 clientes)
- `honorarios.csv` → ejemplo de cuota mensual por cliente
- `costes_gestor.csv` → ejemplo de coste/hora por gestor

Los CSVs son ficticios pero realistas. Puedes ejecutar el prompt tal cual y ver el resultado antes de usar tus datos reales.

---

## Cómo usarlo (5 minutos)

1. **Instala Claude Code** → https://claude.com/claude-code (sigue el instalador oficial, 2 min).

2. **Descomprime este ZIP** en una carpeta local, por ejemplo:
   `C:\Users\tunombre\Downloads\Caso_28_Rentabilidad\`

3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.

4. **Arrastra a Claude Code** este `LEEME.md` y el `prompt.txt` para que la IA entienda el contexto completo antes de ejecutar.

5. **Abre `prompt.txt`**, cambia estas 2 variables al final del prompt:
   - `[EMPRESA]` → el nombre de tu asesoría
   - `[MES AÑO]` → el periodo que analizas (ej: "Septiembre 2026")

6. **Pega el prompt entero** en Claude Code y pulsa Enter.

7. En 1-2 minutos tendrás: dashboard HTML + ranking + propuestas de acción cliente a cliente.

---

## De dónde sacar los datos reales en tu ERP

Si usas tu asesoría con alguno de estos sistemas, estos son los informes a exportar:

| ERP | Horas por cliente | Honorarios | Coste gestor |
|---|---|---|---|
| **A3 Software (Wolters Kluwer)** | A3 Doc → Partes de trabajo | A3 ERP → Facturación recurrente | A3 Nom → Coste empresa / horas útiles |
| **Sage Despachos** | Módulo Gestión Interna → Imputación horaria | Sage → Facturación periódica | Sage Nom → Coste total / horas productivas |
| **Holded** | Proyectos → Timetracking por cliente | Facturación recurrente → Suscripciones | RRHH → Nómina / horas convenio |
| **Odoo** | Hojas de horas → Analítica por cliente | Suscripciones → MRR por cliente | RRHH → Coste empresa |
| **SAP Business One** | Service → Horas por contrato | Contratos de servicio recurrente | HR Add-on → Coste empresa / horas |

Si no tienes imputación horaria, haz una estimación rápida con tus gestores durante 2 semanas. Es suficiente para destapar el 80% de los clientes problemáticos.

---

## Nota importante

Este prompt está diseñado para **asesorías y despachos profesionales** (fiscal, contable, laboral, legal, arquitectura, ingeniería, consultoría). El modelo "cuota recurrente + servicio intensivo en horas" es el que mejor rentabiliza este análisis.

Si tu negocio es por proyectos puntuales (no recurrente), el prompt sigue funcionando pero adapta la variable "mensual" a "por proyecto".

---

*Creado por Isaac Romà · https://isaacroma.com*
