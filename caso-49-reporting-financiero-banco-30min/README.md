# Caso 49 · Reporting financiero para banco en 30 minutos — De 3 días de trabajo a un dossier bancario listo para negociar

> El mismo informe trimestral que tu equipo tarda 3 días en montar (balance, P&L, cash flow y ratios), generado en 30 minutos desde la exportación del ERP.

## 🎯 Problema que resuelve

Cuando el banco pide el informe trimestral, el equipo financiero de una PYME industrial dedica dos o tres días a cuadrar sumas y saldos, montar balance y cuenta de resultados, calcular ratios de endeudamiento y liquidez y preparar el cash flow. Al llegar a la reunión, los datos ya tienen tres semanas, el director de riesgos lo nota y la empresa pierde credibilidad y poder de negociación justo cuando necesita renovar pólizas, pedir más circulante o mejorar condiciones. El problema no es la falta de datos — están todos en el ERP — sino el tiempo de ensamblaje: cada trimestre se reconstruye manualmente el mismo dossier, con el mismo formato y las mismas fórmulas. Este pack usa Claude Code para automatizarlo: lee el balance de sumas y saldos y los movimientos bancarios, construye balance abreviado y cuenta de resultados en formato bancario, deriva cash flow operativo, calcula los ratios que miran los analistas de riesgos (endeudamiento, cobertura, autonomía, liquidez, fondo de maniobra, periodo medio de cobro y pago), compara contra umbrales sectoriales y entrega un dossier HTML visual para la reunión y un Excel de soporte con todos los cálculos trazados. En 30 minutos, con datos de hace horas, no de hace semanas.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía original del caso |
| `prompt.txt` | Prompt para pegar en Claude Code |
| `balance_sumas_saldos.csv` | Ejemplo ficticio (Metalúrgica Pérez S.L.) |
| `movimientos_banco.csv` | Extracto bancario coherente con el balance |

## 🚀 Cómo usarlo en 5 pasos

1. Instala Claude Code siguiendo la guía oficial en https://docs.anthropic.com/en/docs/claude-code y ejecutando `npm install -g @anthropic-ai/claude-code` (requiere Node.js).
2. Crea una carpeta para este caso (ej. `C:\InformeBanco\`) y copia los 4 archivos del ZIP dentro.
3. Abre la terminal en esa carpeta, escribe `claude` y arrastra `LEEME.md` y `prompt.txt` a la conversación para dar contexto completo.
4. Sustituye en el prompt las variables `[EMPRESA]`, `[MES AÑO]` y `@ruta/` por tus datos reales.
5. Pega el prompt y pulsa Enter. En 20-30 minutos tendrás `informe_financiero.html` e `informe_financiero_soporte.xlsx` en la misma carpeta.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Balance de sumas y saldos | Movimientos bancarios |
|---|---|---|
| **SAP Business One** | Finanzas → Informes financieros → Balance de comprobación | Banca → Conciliación → Exportar |
| **Sage 50/200** | Informes → Balances → Sumas y saldos → CSV | Tesorería → Movimientos → CSV |
| **A3 ERP** | Contabilidad → Listados → Sumas y saldos → Exportar | Tesorería → Movimientos bancarios |
| **Holded** | Contabilidad → Informes → Sumas y saldos → Descargar | Tesorería → Cuentas bancarias → CSV |
| **Odoo** | Contabilidad → Informes → Balance general / Sumas y saldos | Contabilidad → Extractos bancarios → Exportar |
| **ContaSOL / ContaPlus** | Informes → Balances → Sumas y saldos | Portal del banco (CSV del extracto) |

Si no exportas desde el ERP, descarga el extracto directamente del portal del banco (Santander, BBVA, CaixaBank, Sabadell, Bankinter — todos permiten CSV). Si las cabeceras no coinciden con los CSV de ejemplo, renómbralas en Excel antes de ejecutar.

> ⚠️ **Nota de sector:** calibrado para PYMEs industriales españolas (fabricación, metalurgia, transformación, mecanizados) de 1-50M€, con los umbrales que miran los analistas de riesgos (endeudamiento < 3,5x, liquidez > 1,2). Si tu empresa es de otro sector (hostelería, construcción, servicios profesionales, retail), pide a Claude Code en el mismo chat que recalibre umbrales. No sustituye a tu asesor fiscal ni al auditor y no presenta cuentas en el Registro Mercantil: es un dossier interno para negociar con el banco. Para cerrar el círculo con la mirada financiera, complementa con [caso-33 (reporting trimestral socios y banco)](../caso-33-reporting-trimestral-socios-banco/), [caso-30 (forecast de tesorería 90 días)](../caso-30-forecast-tesoreria-90-dias/) y [caso-39 (posición financiera por obra)](../caso-39-posicion-financiera-por-obra/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años de C-Suite. Trabajo con PYMEs de 1-50M€ en industria, mayoristas y construcción.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 Reserva 30 min: https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>reporting financiero banco pyme, informe trimestral riesgos bancario, balance y p&l automático desde erp, ratios endeudamiento liquidez pyme industrial, cash flow operativo claude code, dossier negociación póliza crédito, informe financiero 30 minutos, consultor automatización reporting pyme, sumas y saldos a informe bancario, kpis bancarios pyme metalúrgica</sub>
