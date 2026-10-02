# Caso 52 · Informe trimestral de valor entregado al cliente — Convierte tu trabajo invisible en cifras y deja de negociar precio cada trimestre

> El cliente ve una factura de 540 €/mes y no ve las 24 horas invertidas, las 12 declaraciones, las 4 sanciones evitadas ni los 3.400 € que le ahorras frente a un administrativo interno. Este pack lo pone encima de la mesa en PDF.

## 🎯 Problema que resuelve

El cliente de una asesoría no renegocia honorarios porque seas caro, sino porque no percibe el valor que recibe: lo único visible para él es la factura mensual recurrente, mientras que el trabajo real (presentación de modelos, cumplimiento de plazos, resolución de incidencias con Hacienda y Seguridad Social, consultas puntuales, revisión de nóminas) ocurre a puerta cerrada en el despacho. Cuando la asesoría de al lado le ofrece 50 € menos al mes, el cliente no tiene datos para comparar lo que realmente obtiene y por defecto decide por precio. El problema no es el precio: es la ausencia de un relato cuantificado del valor entregado. Este pack usa Claude Code para generar cada trimestre un informe profesional en PDF que convierte servicios, plazos cumplidos, horas invertidas y honorarios facturados en cifras tangibles para el cliente: declaraciones presentadas, porcentaje de cumplimiento de plazos, sanciones y recargos evitados, consultas resueltas, ahorro estimado frente a contratar un administrativo interno a media jornada (≈ 1.100 €/mes) y ROI del servicio sobre honorarios. Se lo mandas al cliente al cierre de cada trimestre con una línea breve y el precio deja de ser el tema de conversación: pasa a serlo el valor demostrado.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía original del caso |
| `prompt.txt` | Prompt para pegar en Claude Code |
| `servicios_cliente.csv` | Servicios prestados en el trimestre |
| `plazos.csv` | Obligaciones y cumplimiento de plazos |
| `honorarios.csv` | Honorarios mensuales facturados |

## 🚀 Cómo usarlo en 5 pasos

1. Instala Claude Code siguiendo la guía oficial en https://docs.anthropic.com/en/docs/claude-code y ejecutando `npm install -g @anthropic-ai/claude-code` (requiere Node.js).
2. Crea una carpeta por cliente y trimestre (ej. `C:\Informes_Clientes\Q1_2026\`) y copia los 3 CSV sustituyendo los datos ficticios por los del cliente real.
3. Abre la terminal en esa carpeta, escribe `claude` y arrastra `LEEME.md` y `prompt.txt` a la conversación.
4. En `prompt.txt`, sustituye `[EMPRESA]` (nombre real del cliente), `[TRIMESTRE AÑO]` (ej. Q1 2026) y `[RUTA]` por tus datos.
5. Pega el prompt y pulsa Enter. En minutos tendrás el PDF listo para enviar al cliente con una línea tipo *"Resumen de lo que hemos hecho por vosotros este trimestre"*.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP de asesoría | Servicios realizados | Plazos cumplidos | Honorarios | Horas invertidas |
|---|---|---|---|---|
| **A3 ASESOR** | Fiscal → Listado modelos presentados | Calendario fiscal → Modelo vs. fecha límite | Facturación → Facturas emitidas | Control de tiempos → Partes |
| **Sage Despachos** | Gestión → Trabajos realizados | Vencimientos → Estado | Facturación → Albaranes/Facturas | Control horario → Imputación cliente |
| **Holded** | Proyectos → Tareas completadas | Tareas → Fecha vencimiento vs. completada | Ventas → Facturas emitidas | Timesheet por proyecto |
| **SAP Business One** | SD → Órdenes de servicio | Workflow → SLA tracking | SD → Billing documents | CATS → Timesheet |
| **Odoo** | Proyectos → Tareas cerradas | Tareas → Fechas límite | Facturación → Facturas de cliente | Hojas de tiempo por cliente |

Si el ERP no exporta directamente a CSV, saca a Excel y guarda como CSV (separador coma, UTF-8). Columnas mínimas: en `servicios_cliente.csv` concepto/modelo, fecha, horas; en `plazos.csv` obligación, fecha límite, fecha real, estado; en `honorarios.csv` mes, importe.

> ⚠️ **Nota de sector:** diseñado para asesorías fiscales, contables y laborales que facturan honorarios mensuales fijos a PYMEs. Si tu modelo es distinto (abogados por horas, consultoría por proyecto, servicios técnicos), cambia "declaraciones" y "plazos fiscales" por los conceptos equivalentes (dictámenes, informes, visitas técnicas) y ajusta el baremo del administrativo interno a tu zona o al perfil que tu cliente tendría que contratar. Para cerrar el bucle de retención y rentabilidad, encadénalo con [caso-46 (liberar horas equipo asesoría)](../caso-46-liberar-horas-equipo-asesoria/), [caso-28 (rentabilidad clientes asesoría)](../caso-28-rentabilidad-clientes-asesoria/) y [caso-40 (rentabilidad por tipo de servicio)](../caso-40-rentabilidad-por-tipo-servicio/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años de C-Suite. Trabajo con PYMEs de 1-50M€ en industria, mayoristas y construcción.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 Reserva 30 min: https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>informe trimestral valor cliente asesoría, retención clientes despacho fiscal, cómo justificar honorarios asesoría, PDF resumen servicios asesor fiscal, ROI servicios despacho profesional, evitar renegociación precio asesoría, informe valor entregado cliente pyme, defensa de precio asesoría contable, automatización reporting cliente asesoría, consultor automatización despachos profesionales</sub>
