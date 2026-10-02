# CASO 31 — Mantenimiento correctivo: las máquinas paran sin avisar

**El problema que resuelve**

Cada hora de máquina parada en una PYME industrial cuesta entre 500€ y 3.000€. Y la mayoría de empresas sigue esperando a que se rompa para repararla. El problema no es que las máquinas fallen — es que fallan siempre igual, por el mismo motivo, con una periodicidad detectable. Pero nadie mira los datos.

Este agente analiza 12 meses de paros no planificados, detecta patrones cíclicos por máquina y causa, calcula el coste acumulado y genera un plan preventivo con fechas, materiales y payback de cada acción. Lo entrega en Excel para el técnico, un dashboard HTML para el gerente y un PDF ejecutivo para dirección.

---

**Qué contiene el ZIP**

- `LEEME.md` — este archivo
- `prompt.txt` — el prompt que pegas en Claude Code
- `paros_12m.csv` — histórico ficticio de 847 paros en 12 meses (10 máquinas de una metalúrgica)
- `maquinas.csv` — catálogo de máquinas con línea, coste/hora de paro y año de instalación

---

**Cómo usarlo**

1. Instala Claude Code: https://claude.ai/code
2. Copia los 2 CSV a una carpeta de tu equipo, por ejemplo `C:\Mantenimiento\` o `~/Mantenimiento/`
3. Abre tu terminal, escribe `claude` y pulsa Enter
4. Arrastra el `LEEME.md` y el `prompt.txt` dentro de la ventana de Claude Code (para que entienda el contexto completo antes de ejecutar)
5. Pega el contenido de `prompt.txt`
6. Cambia estas variables por las tuyas:
   - `[EMPRESA]` → nombre de tu empresa
   - `[MES AÑO]` → periodo analizado (ej. "Octubre 2026")
   - `@ruta/` → la ruta de la carpeta donde están tus CSV
7. Pulsa Enter y espera. Claude Code genera el Excel, el dashboard HTML y el PDF del plan preventivo.

---

**De dónde sacar los datos reales en tu GMAO / ERP**

| Archivo | GMAO Prisma | SAP PM | Fracttal | Mantenimiento Mecalux | Si no tienes GMAO |
|---|---|---|---|---|---|
| `paros_12m.csv` | Informes → Paros no planificados | PM → IW39 órdenes correctivas | Analítica → Órdenes correctivas | Reportes → Averías | Partes de incidencia del encargado de taller en Excel |
| `maquinas.csv` | Maestro activos → Export | PM → IH08 lista equipos | Activos → Export | Equipos → Export | Inventario de máquinas en Excel con coste/hora estimado |

Exporta en **CSV**, separador coma, UTF-8. Si tu GMAO solo te da Excel, ábrelo y guárdalo como CSV.

**Si no tienes GMAO** y los paros se apuntan en papel o en un WhatsApp del encargado, dedica un día a volcarlos a Excel con estas 6 columnas: `fecha, máquina, tipo_paro, causa, duración_horas, coste_estimado`. El retorno de hacerlo una vez bien vale meses.

---

**Nota importante — este prompt está diseñado para industria**

Vale para cualquier PYME industrial con máquinas que fallan: metalurgia, mecanizado, plásticos, alimentación, textil, impresión, carpintería industrial, cerámica. **No vale** para flotas de vehículos (lógica distinta: kilómetros, no fechas), servidores informáticos, o maquinaria agrícola de temporada.

Si tu empresa opera a turnos 24/7, Claude Code lo entenderá si lo indicas en el prompt. Si solo trabajas en turno de día, también.

---

Creado por Isaac Romà · https://isaacroma.com
