# Caso 33 · Reporting trimestral a socios y banco

## El problema que resuelve

En una constructora o promotora PYME, el informe trimestral que se envía a socios o al banco tarda **2–3 días** cada vez. El proceso típico:

- Exportar cartera de obras del ERP (Presto, Menfis, A3 Innuva).
- Sacar balance y P&L del software contable (A3CON, Sage 50, ContaPlus).
- Pedir el estado de certificaciones a administración.
- Pegar todo en Excel, cuadrar, calcular ratios a mano y formatear.
- Montar un PDF o Word con los gráficos.

Resultado: 3 días del gerente o del CFO perdidos cada trimestre. 12 días al año solo en reporting.

Este pack lo resuelve en **15 minutos**: Claude Code lee los CSV, cruza los datos, calcula los ratios bancarios (endeudamiento, liquidez, cobertura de deuda, fondo de maniobra), monta los gráficos de evolución y entrega un informe HTML listo para presentar.

---

## Qué contiene este ZIP

| Archivo | Para qué sirve |
|---|---|
| `LEEME.md` | Este documento. Explica el caso y cómo usarlo. |
| `prompt.txt` | El prompt que pegarás en Claude Code. |
| `obras_activas.csv` | Cartera de 4 obras ficticias: estado, % avance, desviación, backlog. |
| `contabilidad.csv` | Balance, P&L y cash flow trimestralizado. |
| `facturacion_trimestral.csv` | Facturación y margen por obra y por trimestre. |

Los datos son **ficticios pero realistas** (Promociones García S.L., una promotora española tipo). Sirven para que veas el resultado antes de conectarlo a tu empresa real.

---

## Cómo usarlo (paso a paso)

1. **Instala Claude Code** si aún no lo tienes: [claude.com/claude-code](https://claude.com/claude-code)
2. **Descomprime este ZIP** en una carpeta accesible, por ejemplo `~/Descargas/caso_33_reporting_socios/`
3. **Abre tu terminal** (iTerm en Mac, Terminal de Windows) y escribe: `claude`
4. **Arrastra a la ventana de Claude Code** estos tres archivos de contexto:
   - `LEEME.md`
   - `prompt.txt`
   - Los 3 CSV
5. **Abre `prompt.txt`**, cambia la variable `[EMPRESA]` por el nombre de tu empresa y `[MES AÑO]` por el trimestre que quieras reportar.
6. **Pega el prompt en Claude Code** y pulsa Enter.
7. En 10–15 minutos tendrás un HTML listo para abrir en el navegador, imprimir o exportar a PDF.

---

## De dónde sacar los datos reales de tu empresa

Para que funcione con tus datos, exporta estos CSV desde tu ERP o contabilidad:

| CSV | De dónde sacarlo |
|---|---|
| `obras_activas.csv` | **Presto / Menfis / A3 Innuva** → módulo de obras → exportar listado con estado, presupuesto, coste ejecutado, % avance, certificaciones. |
| `contabilidad.csv` | **A3CON / Sage 50 / ContaPlus / Holded** → balance de sumas y saldos + cuenta de resultados por trimestre → exportar a CSV. |
| `facturacion_trimestral.csv` | **Módulo de facturación del ERP** → filtrar por fecha → exportar facturación y coste directo por obra y trimestre. |

Si usas **SAP Business One, Odoo o Microsoft Dynamics**, cualquiera de ellos permite exportar los mismos informes a CSV desde los módulos financieros estándar.

---

## Importante · Prompt diseñado para construcción

Este prompt está pensado para **constructoras, promotoras y empresas de obra civil**. Los ratios y la estructura del informe (certificaciones, backlog, cobertura de deuda sobre EBITDA, desviación de coste por obra) son los que piden socios y bancos en el sector.

Si eres de otro sector (industrial, retail, servicios), el prompt se puede adaptar fácilmente: cambia "obras" por "proyectos" o "líneas de negocio" y ajusta los ratios al estándar de tu sector. Si quieres que lo adapte yo, agenda una reunión en el enlace de abajo.

---

Creado por Isaac Romà · https://isaacroma.com
