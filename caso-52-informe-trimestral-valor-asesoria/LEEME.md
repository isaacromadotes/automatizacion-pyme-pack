# Caso 52 — Informe trimestral de valor entregado al cliente

## El problema que resuelve

Tu cliente negocia tu precio cada trimestre. Te pide descuentos. Compara presupuestos con la asesoría de al lado. No es porque seas caro: es porque **no percibe el valor** que recibe.

El cliente ve una factura de 540€/mes. No ve las 24 horas que invertiste, las 12 declaraciones presentadas, los 4 problemas fiscales que le resolviste antes de que se convirtieran en una sanción, ni los 3.400€ que le ahorras cada trimestre frente a tener un administrativo interno.

Este prompt genera un **informe trimestral de valor entregado** en PDF profesional que convierte tu trabajo invisible en cifras tangibles. Se lo mandas al cliente cada 3 meses. El precio deja de ser el tema.

---

## Qué contiene este ZIP

- **LEEME.md** — este archivo
- **prompt.txt** — el prompt para pegar en Claude Code
- **servicios_cliente.csv** — ejemplo de servicios prestados en el trimestre
- **plazos.csv** — ejemplo de obligaciones y cumplimiento de plazos
- **honorarios.csv** — ejemplo de honorarios mensuales facturados

---

## Cómo usarlo paso a paso

1. **Instala Claude Code** (si aún no lo tienes): sigue las instrucciones en https://docs.claude.com/en/docs/claude-code
2. **Crea una carpeta** en tu equipo, por ejemplo `C:\Informes_Clientes\Q1_2026\`
3. **Copia los 3 CSVs** de este ZIP a esa carpeta
4. **Sustituye los datos ficticios** por los de tu cliente real (mismo formato de columnas)
5. **Abre Claude Code** en esa carpeta
6. **Pega el contenido de `prompt.txt`** y cambia las variables:
   - `[EMPRESA]` → nombre real del cliente (ej: Instalaciones Ruiz S.L.)
   - `[TRIMESTRE AÑO]` → ej: Q1 2026
   - `[RUTA]` → la ruta donde pusiste los CSVs
7. **Pulsa Enter**. Claude Code genera el PDF en minutos
8. **Envía el PDF al cliente** con una línea tipo *"Resumen de lo que hemos hecho por vosotros este trimestre"*

---

## De dónde sacar los datos en tu ERP de asesoría

| Dato | A3 ASESOR | Sage Despachos | Holded | SAP Business One |
|------|-----------|----------------|--------|------------------|
| Servicios realizados | Módulo Fiscal → Listado modelos presentados | Gestión → Trabajos realizados | Proyectos → Tareas completadas | SD → Órdenes de servicio |
| Plazos cumplidos | Calendario fiscal → Modelo presentado vs. fecha límite | Vencimientos → Estado | Tareas → Fecha vencimiento vs. completada | Workflow → SLA tracking |
| Honorarios facturados | Facturación → Listado facturas emitidas | Facturación → Albaranes/Facturas | Ventas → Facturas emitidas | SD → Billing documents |
| Horas invertidas | Control de tiempos → Partes de trabajo | Control horario → Imputación por cliente | Timesheet por proyecto | CATS → Timesheet |

Si tu ERP no exporta directamente a CSV, pide a tu administrador que te saque los datos del trimestre a Excel y guárdalo como CSV (separador coma, codificación UTF-8).

---

## Nota importante

Este prompt está diseñado para **asesorías fiscales, contables y laborales** que facturan honorarios mensuales fijos a PYMEs. Si tu modelo de negocio es diferente (abogados por horas, consultoría por proyecto, servicios técnicos), **adapta el prompt** cambiando las referencias a "declaraciones" y "plazos fiscales" por los conceptos equivalentes de tu sector (dictámenes, informes, visitas técnicas, etc.).

El cálculo de ahorro vs. gestión interna (administrativo media jornada = 1.100€/mes) también puedes ajustarlo a tu baremo local o al perfil que tu cliente tendría que contratar.

---

Creado por Isaac Romà · https://isaacroma.com
