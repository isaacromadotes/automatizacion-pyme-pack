# Caso 39 — Posición financiera por obra (certificaciones vs. cobros)

## El problema que resuelve

Si eres gerente o CFO de una constructora y necesitas llamar a administración para saber **cuánto te deben tus promotores por obra**, tienes un problema de visibilidad.

El resultado: certificaciones que se olvidan en el cajón, vencidos que nadie reclama hasta que ya son impagados, y la tesorería dependiendo de llamadas sueltas.

Este pack monta en minutos un **dashboard de posición financiera por obra**:
certificado · emitido · cobrado · pendiente, con alertas de vencimiento y emails de reclamación auto-generados.

## Qué contiene este ZIP

- `LEEME.md` → este archivo (contexto para que Claude Code entienda el pack)
- `prompt.txt` → el prompt que pegarás en Claude Code
- `certificaciones.csv` → datos de ejemplo con 4 obras y 13 certificaciones
- `promotores.csv` → datos de ejemplo con 4 promotores (contacto + historial de pago)

## Cómo usarlo (5 minutos)

1. **Instala Claude Code** (si no lo tienes): https://claude.com/claude-code
2. **Copia la carpeta completa** del ZIP en una ruta de tu equipo. Ejemplo: `C:\Trabajo\caso_39_cobros_obra\`
3. **Abre terminal en esa carpeta** y escribe: `claude`
4. **Arrastra `LEEME.md` y `prompt.txt` a la ventana de Claude Code** — así entiende el contexto antes de ejecutar
5. **Pega el contenido de `prompt.txt`**, cambia las variables marcadas con `[CORCHETES]` por tus datos, y pulsa Enter
6. Claude Code generará el dashboard web y lo arrancará en tu navegador

## De dónde sacar los datos en tu ERP

Exporta a CSV estos campos desde tu software de gestión:

| Dato | A3 ERP | Sage 50/200 | Holded | SAP B1 | Odoo |
|------|--------|-------------|--------|--------|------|
| Certificaciones | Obras → Certificaciones → Exportar | Proyectos → Certificaciones | Proyectos → Facturación por hitos | Project Management → Progress Billing | Project → Facturación |
| Promotores (clientes) | Maestro Clientes | Clientes → Listado | Contactos → Exportar | Business Partners | Contactos → Clientes |

Si no tienes los campos exactos del CSV de ejemplo, no pasa nada: Claude Code adapta el prompt a las columnas que le pases.

## ⚠️ Nota importante — sector

Este prompt está diseñado para **PYMEs de construcción, obra civil y promoción inmobiliaria** que trabajan por certificaciones mensuales. Si tu modelo es a tanto alzado o facturación directa, dile a Claude Code que ajuste el prompt a tu caso.

## Siguiente paso

Si este ejemplo con datos ficticios te ha resultado útil, imagina lo que puede hacer conectado a los datos reales de tu empresa.

→ Reunión gratuita de 30 min: https://calendly.com/asesor-online-ia/30min
→ Web: https://isaacroma.com
→ Aprende a hacerlo tú: https://isaacroma.com/blog

---

Creado por Isaac Romà · https://isaacroma.com
