# Caso 09 · Partes de obra digitales — Elimina el papel y detecta sobrecostes en tiempo real

> **Resultado clave:** Sustituye los partes en papel por un formulario móvil, imputa horas al tajo correcto el mismo día y detecta desviaciones de MOD cuando aún puedes corregir. Alerta automática al jefe de obra cuando una obra supera el 110% del presupuesto.

## 🎯 Problema que resuelve

En construcción, los partes de trabajo siguen gestionándose en papel: el operario los rellena a medias en el tajo, se guardan arrugados en el bolsillo del mono, llegan el viernes a oficina (si llegan) y alguien los pasa al Excel el lunes siguiente. El resultado es demoledor para el margen: no sabes cuántas horas llevas gastadas en cada obra hasta dos o tres semanas tarde, cuando el sobrecoste ya está consumado y no puedes reaccionar. Las horas acaban imputadas a la obra que "se acuerda" el operario, las certificaciones salen tarde, el flujo de caja se resiente y aparecen discusiones con el cliente por horas que nadie puede justificar. Este caso automatiza el ciclo completo: formulario móvil para que el operario fiche horas por obra/tajo/partida al terminar la jornada, panel del jefe de obra con horas reales vs presupuesto MOD semanal, alerta roja automática al superar el umbral del 110% (estándar del sector), categorías del Convenio General de la Construcción integradas y PDF resumen semanal para dirección. Pensado para constructoras y promotoras españolas de 1-50M€ donde controlar la MOD a tiempo es la diferencia entre obra rentable y obra en pérdida.

## 📦 Archivos del pack

| Archivo | Descripción |
|---------|-------------|
| `LEEME.md` | Instrucciones de uso del caso |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `partes_semana.csv` | Partes de trabajo de una semana (36 registros, 3 obras) |
| `presupuesto_mod.csv` | Presupuesto de mano de obra por obra y semana |
| `obras_activas.csv` | Obras en curso (código, cliente, jefe de obra, presupuesto) |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** si aún no lo tienes: `npm install -g @anthropic-ai/claude-code` (requiere Node.js 18+ y cuenta Anthropic con API key). Guía oficial: [docs.anthropic.com/en/docs/claude-code](https://docs.anthropic.com/en/docs/claude-code)
2. **Copia los 3 CSVs** del pack a una carpeta de tu ordenador (ej: `C:\Users\TU_USUARIO\Downloads\Partes Obra\`).
3. **Abre tu terminal** (CMD, PowerShell o Terminal en Mac) y lanza `claude` desde la carpeta donde están los archivos.
4. **Pega el `prompt.txt`** y antes de pulsar Enter sustituye las variables: `[EMPRESA]` por el nombre de tu constructora, `[SEMANA AÑO]` por el período a analizar (ej. "Semana 37 2026") y `@ruta/` por la ruta real de tus CSVs.
5. **Pulsa Enter y espera**. Claude Code genera formulario móvil para fichar horas, panel del jefe de obra con horas reales vs presupuesto, alerta automática al superar el 110% y PDF resumen semanal para dirección.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Partes de trabajo | Presupuesto MOD | Obras activas |
|-----|-------------------|-----------------|---------------|
| **A3 (A3ERP / A3CON)** | Módulo Obras → Partes de trabajo → Exportar Excel | Obras → Presupuesto MOD semanal | Obras → Maestro obras activas |
| **Sage 50 / Sage 200 Construcción** | Producción → Partes → Listados → Exportar | Presupuestos → MOD → Exportar | Obras → Listado activas |
| **Holded** | Proyectos → Tiempos → Exportar | Proyectos → Presupuesto → Exportar | Proyectos → Listado activos |
| **SAP Business One (PS)** | Transacción CJ74 (horas confirmadas por proyecto) → Exportar | CJ40 → Presupuesto por proyecto | CN41 → Lista de proyectos |
| **Odoo (Project + Timesheets)** | Partes de horas → Filtrar → Descargar | Proyecto → Presupuesto analítico | Proyecto → Listado activos |
| **Presto / Menfis** | Partes de trabajo → Consulta → Exportar CSV | Certificaciones → Presupuesto MOD | Diagrama → Obras activas |

⚠️ **Nota de sector:** Este caso está diseñado específicamente para **constructoras y promotoras españolas** (obra civil, edificación, reformas, instalaciones). Contempla categorías del Convenio General de la Construcción, estructura obra→tajo→partida, presupuesto MOD semanal y umbral de alerta del 110% (estándar del sector). Si tu empresa es **industrial o de servicios**, el prompt sigue funcionando: sustituye "obra" por "proyecto" o "centro de coste" al pegar el prompt y ajusta el umbral de alerta.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con 20 años en C-Suite. Ayudo a PYMEs españolas de **1-50M€** (industria, mayoristas y construcción) a automatizar procesos ejecutivos y traducir operaciones a impacto financiero real (EBITDA, caja, margen).

- **Diagnóstico inicial:** 750€
- **Automatización a medida:** desde 4.500€
- **Acompañamiento mensual:** 300€/mes

👉 **Reserva 30 min gratis:** [calendly.com/asesor-online-ia/30min](https://calendly.com/asesor-online-ia/30min)

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>partes de obra digitales, control MOD construcción, desviación mano de obra PYME constructora, automatización construcción Claude Code, parte trabajo móvil operario, panel jefe de obra, alerta sobrecoste obra, consultor IA construcción España, Convenio General Construcción, control producción obra civil</sub>
