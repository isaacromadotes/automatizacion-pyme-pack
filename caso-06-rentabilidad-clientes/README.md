# Caso 06 · Rentabilidad por cliente — Descubre qué clientes te hacen perder dinero

> **Resultado clave:** Cruza horas reales del equipo con facturación y detecta clientes que facturan mucho pero cuestan más. Caso real del pack: cliente nº2 factura 4.200€/mes y cuesta 5.100€ → pérdida de 900€/mes oculta.

## 🎯 Problema que resuelve

La mayoría de empresas de servicios (consultoras, asesorías, ingenierías, despachos, agencias) facturan por cliente pero nunca cruzan las horas reales de su equipo con lo que cobran. El resultado es demoledor: clientes que parecen estrella por facturación acaban siendo los que más margen destruyen, mientras otros aparentemente pequeños son los verdaderamente rentables. Sin este cruce, las decisiones de precio, renovación de contratos y asignación de equipo se toman a ciegas. Este caso automatiza el análisis de rentabilidad real por cliente (facturación − coste horas equipo), genera un ranking con semáforo verde/ámbar/rojo y entrega recomendaciones concretas: a qué clientes subir precio, cuáles renegociar y cuáles dejar ir. Pensado para PYMEs de servicios profesionales de 1 a 50M€ donde el coste principal es el tiempo del equipo.

## 📦 Archivos del pack

| Archivo | Descripción |
|---------|-------------|
| `LEEME.md` | Instrucciones de uso del caso |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `horas_equipo.csv` | Horas mensuales por empleado y cliente |
| `costes_empleado.csv` | Coste/hora y rol de cada empleado |
| `facturacion_clientes.csv` | Facturación mensual por cliente y tipo de contrato |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** si aún no lo tienes: `npm install -g @anthropic-ai/claude-code` (requiere Node.js 18+ y cuenta Anthropic con API key). Guía oficial: [docs.anthropic.com/en/docs/claude-code](https://docs.anthropic.com/en/docs/claude-code)
2. **Copia los 3 CSVs** del pack a una carpeta de tu ordenador (ej: `C:\Users\TU_USUARIO\Downloads\Rentabilidad\`).
3. **Abre tu terminal** (CMD, PowerShell o Terminal en Mac) y lanza `claude` desde la carpeta donde están los archivos.
4. **Pega el `prompt.txt`** y antes de pulsar Enter sustituye las variables: `[EMPRESA]` por el nombre de tu empresa, `[MES AÑO]` por el período a analizar y `@ruta/` por la ruta real de tus CSVs.
5. **Pulsa Enter y espera**. Claude Code cruza los tres archivos, calcula rentabilidad por cliente y genera un dashboard HTML interactivo con semáforo, ranking y recomendaciones de acción.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Horas equipo | Costes empleado | Facturación clientes |
|-----|--------------|-----------------|----------------------|
| **A3 (A3 Gestión / A3 Asesor)** | Control horario → Informe horas por empleado/proyecto | Módulo nóminas → Coste empresa/hora | Facturación → Informe por cliente y período |
| **Sage 200** | Partes de trabajo → Exportar por cliente/empleado | Nóminas Sage → Coste hora | Ventas → Informe facturación por cliente |
| **Holded** | Gestión del tiempo → Informe por proyecto/cliente | RRHH → Coste empresa por empleado | Facturación → Informe cliente/mes |
| **SAP Business One** | Módulo Proyectos → Informe actividades | HR module → Labor cost per employee | Ventas → Informe facturación cliente |
| **Odoo** | Hojas de tiempo → Exportar CSV por cliente | Nómina → Coste empleado/hora | Contabilidad → Facturas emitidas por cliente |

⚠️ **Nota de sector:** Este caso está diseñado para **empresas de servicios profesionales** (consultoras, asesorías, despachos, ingenierías, agencias) donde el coste principal es el tiempo del equipo. Si tu empresa es **industrial o mayorista**, la rentabilidad por cliente requiere incluir materiales, coste de producción y márgenes por producto — en ese caso usa el **Caso 19 · Margen por producto** o contacta para adaptarlo.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con 20 años en C-Suite. Ayudo a PYMEs españolas de **1-50M€** (industria, mayoristas y construcción) a automatizar procesos ejecutivos y traducir operaciones a impacto financiero real (EBITDA, caja, margen).

- **Diagnóstico inicial:** 750€
- **Automatización a medida:** desde 4.500€
- **Acompañamiento mensual:** 300€/mes

👉 **Reserva 30 min gratis:** [calendly.com/asesor-online-ia/30min](https://calendly.com/asesor-online-ia/30min)

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>rentabilidad por cliente PYME, análisis clientes no rentables, consultoría automatización PYME, Claude Code España, consultor IA PYME, EBITDA por cliente, control horas equipo consultora, margen cliente servicios profesionales, automatización financiera PYME, dashboard rentabilidad clientes</sub>
