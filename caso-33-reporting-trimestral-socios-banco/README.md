# Caso 33 · Reporting trimestral a socios y banco — De 3 días a 15 minutos cada trimestre

> **Resultado:** 12 días del gerente o CFO al año recuperados. Informe HTML listo para socios y banco con ratios bancarios, gráficos de evolución y desviación por obra en 10-15 minutos.

## 🎯 Problema que resuelve

En una constructora o promotora PYME el informe trimestral que se envía a socios o al banco se come 2-3 días cada vez. El proceso típico es siempre el mismo: exportar cartera de obras del ERP (Presto, Menfis, A3 Innuva), sacar balance y P&L del software contable (A3CON, Sage 50, ContaPlus), pedir el estado de certificaciones a administración, pegar todo en Excel, cuadrar manualmente, calcular ratios bancarios con fórmulas que nadie recuerda del trimestre anterior y montar un PDF o Word con gráficos a mano. Resultado: 3 días del gerente o del CFO perdidos cada trimestre, 12 días al año solo en reporting, informes que llegan tarde al comité de riesgos del banco y datos que no cuadran entre un trimestre y el siguiente porque cada vez los calcula una persona distinta con un criterio distinto. El coste real no son solo las horas: son peores condiciones de financiación cuando el banco percibe falta de control, socios con menos visibilidad para decidir ampliaciones de capital y un gerente atrapado en Excel en vez de en obra. Este caso automatiza el cruce de cartera de obras, contabilidad trimestralizada y facturación por obra, calcula los ratios bancarios estándar del sector (endeudamiento, liquidez, cobertura de deuda sobre EBITDA, fondo de maniobra, desviación de coste por obra, backlog), monta los gráficos de evolución y entrega un informe HTML listo para presentar, imprimir o exportar a PDF.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `obras_activas.csv` | Cartera de 4 obras ficticias con estado, % avance, desviación, backlog |
| `contabilidad.csv` | Balance, P&L y cash flow trimestralizado |
| `facturacion_trimestral.csv` | Facturación y margen por obra y por trimestre |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_33_Reporting_Socios\`) con los 3 CSVs en la raíz.
3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md`, `prompt.txt` y los 3 CSVs** al chat para dar contexto completo antes de ejecutar.
5. **Edita `prompt.txt`** sustituyendo `[EMPRESA]` por el nombre de tu empresa y `[MES AÑO]` por el trimestre a reportar, pégalo y pulsa Enter. En 10-15 minutos tendrás un HTML listo para presentar o exportar a PDF.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP / Software | Obras activas | Contabilidad trimestral | Facturación por obra |
|---|---|---|---|
| **Presto** | Módulo obras → Export listado con % avance y desviación | — (combinar con software contable) | Certificaciones por obra |
| **CYPE** | Gestión de obra → Export estado y backlog | — (combinar con software contable) | Certificaciones por obra |
| **Menfis** | Obras → Export cartera activa | — (combinar con software contable) | Facturación por obra |
| **A3 Innuva / A3CON** | Módulo obras → Cartera activa | A3CON → Balance + P&L trimestral | Facturación por obra/centro |
| **Sage 50 / Sage 200 Construcción** | Módulo obras → Export estado | Balance + P&L trimestral | Facturación por obra |
| **Holded** | Proyectos → Export estado y margen | Balance + P&L por periodo | Facturación por proyecto |
| **SAP Business One / Odoo / MS Dynamics** | Módulo proyectos → Export | Finanzas → Informes financieros | Facturación por proyecto |
| **Contasol / ContaPlus** | — (combinar con módulo de obras) | Balance de sumas y saldos + P&L trimestral | Facturación por centro |

> ⚠️ **Nota de sector:** Diseñado para **constructoras, promotoras y empresas de obra civil**. Los ratios (certificaciones, backlog, cobertura de deuda sobre EBITDA, desviación de coste por obra) son los que piden socios y bancos en el sector. Si eres de industria, retail o servicios, cambia "obras" por "proyectos" o "líneas de negocio" y ajusta los ratios al estándar sectorial. Para el detalle de tesorería que acompaña a este reporting, combina con [caso-30 (forecast tesorería 90 días)](../caso-30-forecast-tesoreria-90-dias/) o [caso-32 (forecast tesorería mayorista)](../caso-32-forecast-tesoreria-mayorista/) según perfil del negocio.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>reporting trimestral constructora, informe socios banco promotora, ratios bancarios endeudamiento cobertura deuda EBITDA, Claude Code reporting financiero, cuadro mando constructora PYME, certificaciones backlog obra civil, automatización CFO construcción, desviación coste obra ERP Presto Menfis, informe trimestral A3CON Sage, consultoría automatización PYME construcción España</sub>
