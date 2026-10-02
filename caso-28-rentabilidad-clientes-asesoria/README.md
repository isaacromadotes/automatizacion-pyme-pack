# Caso 28 · Rentabilidad real por cliente en asesoría — Detecta en 30 segundos qué clientes te hacen perder dinero

> **Resultado:** Identifica el % de cartera con margen negativo cruzando horas reales, honorarios y coste/hora de gestor. Plan de acción cliente a cliente (subir precio, limitar scope o reestructurar) en 1-2 minutos.

## 🎯 Problema que resuelve

Una asesoría media gestiona cientos de clientes bajo cuota mensual fija, pero prácticamente ninguna sabe cuánto cuesta de verdad atender a cada uno. Entre consultas telefónicas no facturadas, rectificaciones de IVA de última hora, dudas constantes por WhatsApp, expedientes complejos que consumen horas de socio y clientes "históricos" con tarifas congeladas desde hace años, se acumula una capa invisible de clientes deficitarios que erosionan el margen del despacho mes a mes. El síntoma típico es un despacho con facturación creciente pero rentabilidad plana o decreciente, socios saturados y gestores quemados atendiendo a los mismos clientes de siempre sin saber por qué no sale la cuenta. Este caso cruza en un solo análisis las horas reales imputadas por cliente y gestor, los honorarios recurrentes cobrados y el coste/hora real de cada profesional (incluyendo cargas sociales y horas útiles), devolviendo un ranking de rentabilidad real, un dashboard visual del porcentaje de cartera con margen negativo y una propuesta concreta por cada cliente problemático: subida de tarifa justificada, limitación de scope o reestructuración del servicio. Es el primer paso para pasar de facturar más a ganar más.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `horas_cliente.csv` | Ejemplo de horas imputadas por cliente/gestor (20 clientes) |
| `honorarios.csv` | Ejemplo de cuota mensual por cliente |
| `costes_gestor.csv` | Ejemplo de coste/hora por gestor |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_28_Rentabilidad\`) y abre la terminal en esa ruta.
3. **Arranca Claude Code** escribiendo `claude` en la terminal y arrastra el `LEEME.md` y el `prompt.txt` a la ventana para dar contexto.
4. **Edita `prompt.txt`** y sustituye `[EMPRESA]` por el nombre de tu asesoría y `[MES AÑO]` por el periodo a analizar (ej. "Septiembre 2026").
5. **Pega el prompt completo** en Claude Code y pulsa Enter. En 1-2 minutos obtendrás dashboard HTML, ranking de rentabilidad y acciones concretas por cliente.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Horas por cliente | Honorarios | Coste gestor |
|---|---|---|---|
| **A3ASESOR (Wolters Kluwer)** | A3 Doc → Partes de trabajo por expediente | A3 ERP → Facturación recurrente / cuotas | A3 Nom → Coste empresa / horas útiles |
| **Sage Despachos** | Gestión Interna → Imputación horaria | Facturación periódica → Suscripciones | Sage Nom → Coste total / horas productivas |
| **Holded** | Proyectos → Timetracking por cliente | Facturación recurrente → Suscripciones | RRHH → Nómina / horas convenio |
| **Odoo** | Hojas de horas → Analítica por cliente | Suscripciones → MRR por cliente | RRHH → Coste empresa |
| **SAP Business One** | Service → Horas por contrato | Contratos de servicio recurrente | HR Add-on → Coste empresa / horas |
| **Contasol / ContaPlus** | No nativo (usa Excel paralelo o módulo de gestión) | Facturación → Clientes recurrentes | Nóminas → Coste empresa mensual |

> ⚠️ **Nota de sector:** Este caso está pensado para **asesorías fiscales, contables, laborales, despachos de abogados, arquitectura, ingeniería y consultoría** — negocios con cuota recurrente + servicio intensivo en horas. Si tu asesoría no imputa horas, haz una estimación rápida con tus gestores durante 2 semanas: basta para destapar el 80% de los clientes problemáticos. Si trabajas por proyectos puntuales en vez de cuota, sustituye la variable "mensual" por "por proyecto". Complementa con [caso-XX (análisis de cartera comercial)](../caso-XX-slug/) cuando toque priorizar subidas de tarifa por cliente.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** (y despachos profesionales) a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>rentabilidad clientes asesoría, análisis margen despacho profesional, coste real por cliente asesoría fiscal, automatización despacho contable con IA, Claude Code para asesorías, imputación horaria A3ASESOR, cartera clientes deficitarios asesoría, subida honorarios asesoría fiscal, control gestión despacho profesional, consultoría automatización PYME España</sub>
