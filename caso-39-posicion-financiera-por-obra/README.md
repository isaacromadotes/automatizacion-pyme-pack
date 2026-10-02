# Caso 39 · Posición financiera por obra — Dashboard de certificaciones vs. cobros con alertas y reclamaciones

> **Resultado:** Dashboard web con certificado · emitido · cobrado · pendiente por obra, alertas de vencimiento automáticas y emails de reclamación generados. Fin de las certificaciones olvidadas en el cajón y los impagos detectados cuando ya es tarde.

## 🎯 Problema que resuelve

En una constructora o promotora PYME el gerente o CFO tiene que llamar a administración cada vez que quiere saber cuánto le deben los promotores por cada obra activa, porque no existe una visión unificada en tiempo real. La información está fragmentada: las certificaciones mensuales se emiten desde el módulo de obra, las facturas desde contabilidad, los cobros se registran en el banco y las reclamaciones viven en la cabeza del administrativo que lleva años tratando con cada promotor. El resultado es una secuencia que se repite mes a mes: certificaciones aprobadas que se olvidan en el cajón porque nadie recordó facturarlas, facturas vencidas a 60 o 90 días que no se reclaman hasta que el promotor abre otro frente contractual, descuentos de última hora que se aceptan por desconocer la antigüedad real del saldo y una tesorería que depende de llamadas sueltas al promotor de turno en vez de un sistema de reclamación estructurado. En construcción, donde el margen por obra es estrecho y cada punto de DSO adicional come caja operativa, este descontrol significa pagar póliza de crédito evitable e incluso dejar de licitar obras rentables por falta de liquidez. Este caso automatiza el cruce de certificaciones emitidas, facturas registradas y cobros confirmados, calcula la posición financiera real por obra y por promotor, lanza alertas de vencimiento con antelación configurable y genera emails de reclamación personalizados listos para enviar con el tono adecuado según historial de pago del promotor.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `certificaciones.csv` | Datos de ejemplo con 4 obras y 13 certificaciones |
| `promotores.csv` | Datos de ejemplo con 4 promotores (contacto + historial de pago) |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_39_Certificaciones\`) con los 2 CSVs en la raíz.
3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md`, `prompt.txt` y los 2 CSVs** al chat para dar contexto antes de ejecutar.
5. **Edita `prompt.txt`** sustituyendo las variables entre `[CORCHETES]`, pégalo y pulsa Enter. Claude Code generará el dashboard web y lo arrancará en el navegador.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Certificaciones por obra | Promotores (clientes) |
|---|---|---|
| **Presto** | Certificaciones mensuales → Export | — (combinar con software contable) |
| **CYPE** | Gestión obra → Certificaciones → Export | — (combinar con software contable) |
| **Menfis** | Obras → Certificaciones → Export | Maestro de promotores |
| **A3 Innuva / A3 ERP** | Obras → Certificaciones → Export | Maestro clientes |
| **Sage 50 / Sage 200 Construcción** | Proyectos → Certificaciones | Clientes → Listado |
| **Holded** | Proyectos → Facturación por hitos | Contactos → Export |
| **SAP Business One** | Project Management → Progress Billing | Business Partners |
| **Odoo** | Project → Facturación por hitos | Contactos → Clientes |
| **Contasol / ContaPlus** | — (combinar con módulo obras) | Maestros → Clientes |

Si tu ERP no entrega el CSV con las columnas exactas del ejemplo, Claude Code adapta el prompt a las columnas que le pases.

> ⚠️ **Nota de sector:** Diseñado para **PYMEs de construcción, obra civil, reformas industriales y promoción inmobiliaria** que facturan por certificaciones mensuales. Si tu modelo es a tanto alzado, hito único o facturación directa sin certificaciones, pide a Claude Code que ajuste el prompt. Para el reporting trimestral que acompaña esta posición financiera por obra, combina con [caso-33 (reporting trimestral socios y banco)](../caso-33-reporting-trimestral-socios-banco/); para enlazar impagos con tensión de caja global, con [caso-30 (forecast tesorería 90 días)](../caso-30-forecast-tesoreria-90-dias/).

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>posición financiera por obra constructora, certificaciones vs cobros promotor, control impagados obra civil, DSO certificaciones construcción, Claude Code gestión cobros obra, dashboard certificaciones mensuales, reclamación promotor automatizada, Presto CYPE Menfis certificaciones, CFO constructora PYME, consultoría automatización construcción España</sub>
