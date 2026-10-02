# Caso 27 — Tesorería mezclada entre obras

## El problema que resuelve

Tu empresa tiene varias obras abiertas al mismo tiempo. La tesorería está mezclada en una sola cuenta y el consolidado parece sano, pero no sabes **qué obra genera caja** y **cuál la consume**.

Resultado: una obra buena puede estar financiando a una mala sin que lo veas. Decides sobre tu negocio a ciegas.

**Este pack separa la tesorería por obra**, identifica obras que drenan caja, detecta cuáles están financiando a otras, y genera un panel ejecutivo + Excel + informe HTML profesional en minutos.

---

## Qué contiene este ZIP

- `LEEME.md` — este archivo
- `prompt.txt` — el prompt listo para pegar en Claude Code
- `cobros_obra.csv` — cobros reales de 4 obras (datos ficticios de ejemplo)
- `pagos_obra.csv` — pagos reales de las 4 obras
- `certificaciones_pendientes.csv` — certificaciones emitidas pendientes de cobro

---

## Cómo usarlo paso a paso

**1. Instala Claude Code** (si aún no lo tienes)
   - Windows: https://docs.anthropic.com/en/docs/claude-code
   - Necesitas Node.js 18 o superior

**2. Descomprime este ZIP** en una carpeta de tu equipo.
   Ejemplo: `C:\Users\tu_usuario\Downloads\caso_27_tesoreria_obras\`

**3. Sustituye los CSVs de ejemplo por los tuyos** (opcional).
   Si quieres probarlo con tus datos reales, exporta los tuyos de tu ERP y mantén la misma estructura de columnas.

**4. Abre la terminal** en esa carpeta y escribe: `claude`

**5. Arrastra el `LEEME.md` y el `prompt.txt` a la terminal de Claude Code**, junto con los 3 CSVs.
   Esto le da a Claude todo el contexto antes de ejecutar.

**6. Pega el contenido de `prompt.txt`** en la terminal.

**7. Cambia las variables entre corchetes**:
   - `[EMPRESA]` → nombre de tu constructora
   - `[MES AÑO]` → el mes y año que analizas (ej: Octubre 2026)
   - `[RUTA]` → la ruta donde están tus CSVs

**8. Pulsa Enter** y deja que Claude Code trabaje. Al terminar, abrirá el panel web automáticamente.

---

## De dónde sacar los datos en tu ERP

- **Sage 50/200 / A3 Innuva**: módulo de contabilidad → extractos por centro de coste (cada obra = un centro de coste)
- **Holded**: Proyectos → cada obra como proyecto → exportar cobros y pagos filtrados
- **SAP B1**: WBS/elementos PEP por obra → informe de flujo de caja por proyecto
- **Odoo**: Proyectos / Cuentas analíticas → informe analítico por obra
- **Excel manual**: si no tienes ERP, pide a tu contable el extracto bancario separado por obra o monta un libro con una columna "obra" en cada movimiento

Si tu constructora **no tiene imputación por obra**, este es el primer paso que debes corregir. Sin eso, es imposible saber qué obra te hace ganar dinero.

---

## ⚠️ Nota importante

Este prompt está diseñado para **constructoras y promotoras españolas** con 2 o más obras simultáneas. Funciona igual para:

- Instaladoras con varios proyectos en paralelo
- Reformas con 3+ clientes activos
- Industriales con pedidos grandes separados por centro de coste

**NO está pensado para**: empresas con una sola obra/proyecto activo, servicios recurrentes sin imputación por cliente, o distribución mayorista.

---

Creado por Isaac Romà · https://isaacroma.com
