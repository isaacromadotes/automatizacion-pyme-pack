# Caso 31 · Mantenimiento correctivo: las máquinas paran sin avisar — Pasa de reaccionar a prevenir con 12 meses de datos

> **Resultado:** Cada hora de máquina parada en una PYME industrial cuesta entre 500€ y 3.000€. Este agente detecta patrones cíclicos en 12 meses de paros no planificados, calcula el coste acumulado y genera un plan preventivo con fechas, materiales y payback por acción.

## 🎯 Problema que resuelve

En la mayoría de PYMEs industriales las máquinas siguen funcionando bajo lógica correctiva pura: se espera a que se rompan para repararlas. El problema no es que fallen —toda máquina falla—, sino que fallan siempre igual, por la misma causa raíz y con una periodicidad perfectamente detectable si alguien se parara a mirar los datos. Pero nadie lo hace: el encargado de taller apaga fuegos, el gerente ve un coste de mantenimiento disperso en diez partidas distintas y nadie cruza histórico de paros con coste/hora de línea, piezas afectadas y materiales recurrentes. El resultado es una PYME metalúrgica, de mecanizado, plásticos o alimentación perdiendo entre 30.000 € y 200.000 € al año en paros evitables, con el OEE estancado y el equipo de producción quemado. Este caso automatiza el análisis de 12 meses de paros no planificados, cruza datos con el catálogo de máquinas (línea, coste/hora de paro, año de instalación), detecta patrones cíclicos por máquina y causa raíz, calcula el coste acumulado por tipo de avería y devuelve tres entregables listos para usar: Excel operativo para el técnico de mantenimiento, dashboard HTML para el gerente y PDF ejecutivo para dirección con el payback de cada acción preventiva propuesta.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `paros_12m.csv` | Histórico ficticio de 847 paros en 12 meses (10 máquinas metalúrgicas) |
| `maquinas.csv` | Catálogo de máquinas con línea, coste/hora de paro y año de instalación |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_31_Mantenimiento\`) con los 2 CSVs en la raíz.
3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md`, `prompt.txt` y los 2 CSVs** al chat para dar contexto antes de ejecutar.
5. **Edita `prompt.txt`** cambiando `[EMPRESA]`, `[MES AÑO]` y la ruta `@ruta/`, pégalo y pulsa Enter. Obtendrás Excel operativo + dashboard HTML + PDF ejecutivo con el plan preventivo.

## 🔌 Cómo exportar los datos desde tu GMAO / ERP

| Sistema | Paros 12 meses | Catálogo de máquinas |
|---|---|---|
| **SAP PM** | Transacción IW39 → Órdenes correctivas | Transacción IH08 → Lista de equipos |
| **GMAO Prisma** | Informes → Paros no planificados | Maestro de activos → Export |
| **Fracttal** | Analítica → Órdenes correctivas | Activos → Export CSV |
| **Mantenimiento Mecalux** | Reportes → Averías | Equipos → Export |
| **A3 ERP (Wolters Kluwer)** | Módulo producción → Partes de incidencia | Maestro de recursos productivos |
| **Sage 200 / Holded / Odoo** | Módulo MRP → Paros registrados en órdenes de fabricación | Fabricación → Centros de trabajo |

Exporta siempre en **CSV, separador coma, UTF-8**. Si tu sistema solo da Excel, ábrelo y guárdalo como CSV antes de pasarlo a Claude Code.

> ⚠️ **Nota de sector:** Diseñado para **PYMEs industriales** con máquinas que fallan: metalurgia, mecanizado, plásticos, alimentación, textil, impresión, carpintería industrial, cerámica. **No vale** para flotas de vehículos (lógica por kilómetros, no fechas), servidores informáticos o maquinaria agrícola de temporada. Si operas a turnos 24/7, indícalo en el prompt. Si no tienes GMAO y los paros se apuntan en papel o en WhatsApp del encargado, dedica un día a volcarlos a Excel con 6 columnas: `fecha, máquina, tipo_paro, causa, duración_horas, coste_estimado` — el retorno vale meses. Para enlazar el impacto en coste de producto, complementa con [caso-29 (coste real por referencia)](../caso-29-coste-real-gran-distribucion/).

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>mantenimiento preventivo PYME industrial, análisis paros no planificados máquinas, reducir coste hora parada producción, GMAO SAP PM Fracttal Prisma, plan mantenimiento correctivo con IA, OEE PYME metalúrgica, Claude Code mantenimiento industrial, patrones averías cíclicas máquinas, payback mantenimiento preventivo, consultoría automatización industria España</sub>
