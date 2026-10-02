# Caso 03 · Control de Costes de Obra en Tiempo Real — Sabe si ganas o pierdes antes de acabar

> Pack listo para implementar en constructoras y promotoras españolas. Resultado: cuadro de control con semáforo por partida, proyección de coste final y alertas automáticas en minutos, no en semanas.

## 🎯 Problema que resuelve

En la mayoría de constructoras y promotoras, el control de costes se hace en un Excel que "alguien actualiza cuando tiene tiempo". El resultado: no sabes si la obra gana o pierde dinero hasta que termina — y cuando termina, ya no puedes hacer nada. Este pack cruza presupuesto, ejecución real y certificaciones para darte un dashboard con desviaciones por partida, proyección de coste final y alertas en rojo/amarillo/verde.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía original del caso |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `presupuesto_obra.csv` | Presupuesto por partida (obra ejemplo: 1,2M€) |
| `costes_reales.csv` | Costes ejecutados por partida con % de avance |
| `certificaciones.csv` | Certificaciones mensuales y cobros |

## 🚀 Cómo usarlo en 5 pasos

1. **Descarga** los archivos de esta carpeta.
2. **Abre** `prompt.txt` y cópialo.
3. **Pégalo** en Claude Code ([instalación aquí](https://docs.anthropic.com/en/docs/claude-code)).
4. **Cambia** `[EMPRESA]`, `[NOMBRE OBRA]`, `[MES AÑO]` y `@ruta/` por tus datos reales.
5. **Pulsa Enter**: Claude Code genera dashboard web interactivo + PDF para dirección con semáforos y alertas.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Presupuesto | Costes reales | Certificaciones |
|---|---|---|---|
| **A3 Construcción / A3CON** | Presupuestos → Exportar partidas | Certificaciones → Costes reales por partida | Certificaciones mensuales → Exportar |
| **Presto** | Archivo presupuesto → CSV | Seguimiento económico → Ejecución | Certificaciones → Resumen mensual |
| **Sage Despachos / ContaPlus** | Obras → Presupuesto por capítulos | Analítica → Costes por centro (obra) | Facturación → Certificaciones emitidas |
| **Odoo (construcción)** | Proyecto → Presupuesto → Exportar | Partes de obra → Costes ejecutados | Facturación proyecto |
| **SAP Business One** | Proyectos → Presupuesto → Exportar | Controlling → Costes reales por PEP | Facturas emitidas filtradas por obra |

⚠️ **Diseñado para construcción, promoción y rehabilitación** (partidas, certificaciones, semáforo de desviación son estándar del sector). Para otros sectores con control de proyecto, hay que adaptar.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con 20 años en C-Suite. Ayudo a PYMEs españolas (1-50M€) de industria, mayoristas y construcción a automatizar su gestión con IA.

**Servicios:**
- 🔍 **Diagnóstico de automatización**: 750€
- ⚙️ **Automatización llave en mano**: desde 4.500€
- 🤝 **Acompañamiento mensual**: 300€/mes

👉 **Reserva 30 min gratis**: [calendly.com/asesor-online-ia/30min](https://calendly.com/asesor-online-ia/30min)

---

**Isaac Romà** · Consultor de automatización IA para PYMEs
🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://linkedin.com/in/isaacroma) · 💻 [GitHub](https://github.com/isaacromadotes)

---

<sub>**Keywords**: control costes obra tiempo real, dashboard construcción PYME, Claude Code constructora, semáforo desviación partidas, proyección coste final obra, Presto automatización, A3 Construcción integración IA, control económico obra, certificaciones automatizadas, consultor automatización construcción España.</sub>
