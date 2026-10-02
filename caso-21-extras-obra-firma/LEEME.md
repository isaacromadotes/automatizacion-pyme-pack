# Caso 21 · Extras de obra acordados de palabra que no se cobran

## El problema que resuelve

En construcción, los extras de obra se acuerdan **de palabra** entre el jefe de obra y el cliente en la propia obra. Después de dos meses, cuando llega la factura, el cliente responde: "**yo no aprobé eso**". Y el extra se asume como coste.

Una obra media pierde entre **8.000 € y 25.000 € al año** solo en extras no cobrados: cambios de material, tabiques nuevos, puntos de luz añadidos, refuerzos estructurales tras cata, ampliaciones de última hora... Todo lo que se ejecuta sin firma se paga con tu margen.

Este pack te da el flujo completo que resuelve el problema:

1. El jefe de obra registra el extra desde el móvil (descripción, medición, fotos, urgencia).
2. Se genera el presupuesto automático con los precios unitarios del contrato original.
3. El cliente recibe un documento de aprobación con firma digital.
4. **Si no firma, no se ejecuta.**
5. Todo queda registrado en un dashboard con el acumulado por obra.

## Qué contiene el ZIP

- **LEEME.md** — Este archivo.
- **prompt.txt** — El prompt listo para pegar en Claude Code.
- **precios_contrato.csv** — 20 unidades de obra con precios unitarios del contrato original (albañilería, electricidad, fontanería, pintura, carpintería, climatización, impermeabilización, estructura, seguridad).
- **extras_obra_mirador.csv** — 14 extras reales de la obra "Residencial Mirador" con fechas, mediciones, estados (aprobado/pendiente/rechazado) e importes.
- **obras_activas.csv** — 5 obras activas de una constructora con presupuesto original y extras acumulados por estado.

## Cómo usarlo paso a paso

1. **Instala Claude Code** (si aún no lo tienes): sigue las instrucciones en https://claude.com/claude-code
2. **Copia esta carpeta completa** a tu ordenador. Ruta recomendada: `C:\Users\[tu_usuario]\Downloads\Caso 21 Extras de obra\`
3. **Abre una terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Abre `prompt.txt`** con cualquier editor de texto y cambia las variables:
   - `[EMPRESA]` → nombre de tu constructora
   - `[MES AÑO]` → mes y año actual (ej. "Septiembre 2026")
   - `@ruta/` → ruta absoluta de esta carpeta en tu ordenador
5. **Copia el prompt completo** y pégalo en Claude Code.
6. **Pulsa Enter** y deja que Claude Code genere el sistema completo. Al terminar arranca un servidor local que puedes abrir en el navegador.

## De dónde sacar los datos en tu ERP

- **Precios de contrato:** exporta las unidades de obra con precio unitario desde tu programa de presupuestos:
  - **Presto** → menú Archivo > Exportar > Excel (columnas: código, resumen, precio, ud)
  - **Arquímedes / CYPE** → Listados > Exportar mediciones y presupuesto
  - **Menfis** → Utilidades > Exportar a Excel
  - **SAP PS / Módulo Proyectos** → transacción CJ20N → exportar estructura del proyecto
  - **Sage 200 Construcción** → Informes de presupuesto por partida
- **Extras acumulados:** habitualmente están en el parte diario del jefe de obra o en un Excel paralelo. Si aún no los llevas centralizados, este pack te sirve como plantilla de arranque.
- **Obras activas:** tu programa de gestión de obra o el sistema de facturación (Sage, A3ERP, Holded, Odoo).

## Nota importante

Este prompt está diseñado para el **sector construcción** (obra nueva y reforma), pero el flujo de "trabajo adicional acordado de palabra → presupuesto → firma → facturación" es aplicable con adaptaciones a:

- **Talleres mecánicos** (reparaciones adicionales tras diagnóstico).
- **Servicios técnicos e instalaciones** (mantenimiento correctivo).
- **Consultoría por horas** (alcance añadido).
- **Estudios de arquitectura e ingeniería** (modificaciones de proyecto).

Si tu caso es alguno de estos, dile a Claude Code que adapte los términos del prompt a tu sector.

---

Creado por Isaac Romà · https://isaacroma.com
