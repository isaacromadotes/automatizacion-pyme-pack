# VÍDEO 49 — Reporting financiero para banco en 30 minutos

## El problema que resuelve

Tu banco te pide el informe trimestral: balance, cuenta de resultados, cash flow y ratios. Tu equipo tarda 3 días en montarlo. Cuando llegas a la reunión, los datos ya tienen 3 semanas. Pierdes credibilidad y poder de negociación.

Este pack te permite generar el mismo informe — en formato bancario — en **30 minutos**, directamente desde los datos que exporta tu ERP.

## Qué contiene este ZIP

- `LEEME.md` — este archivo
- `prompt.txt` — el prompt que pegarás en Claude Code
- `balance_sumas_saldos.csv` — ejemplo ficticio de una metalúrgica (Metalúrgica Pérez S.L.)
- `movimientos_banco.csv` — extracto bancario coherente con el balance

## Cómo usarlo (5 pasos)

1. **Instala Claude Code** si aún no lo tienes: https://docs.claude.com/en/docs/claude-code
2. **Crea una carpeta** en tu equipo para este caso (ej. `C:\InformeBanco\`) y copia los 4 archivos del ZIP dentro.
3. **Abre la terminal** en esa carpeta y escribe `claude`.
4. **Arrastra a la terminal** este `LEEME.md` y el `prompt.txt` (así Claude Code tiene el contexto completo del caso antes de ejecutar).
5. **Pega el prompt** de `prompt.txt`, cambia las variables `[EMPRESA]`, `[MES AÑO]` y `@ruta/` por los tuyos, y pulsa Enter.

En 20-30 minutos tendrás el `informe_financiero.html` y el `informe_financiero_soporte.xlsx` listos en la misma carpeta.

## De dónde sacar los datos en tu ERP

El prompt usa dos entradas estándar que **todos** los ERPs exportan:

- **Balance de sumas y saldos** (CSV o Excel):
  - A3 ERP → Contabilidad → Listados → Balance de sumas y saldos → Exportar
  - Sage 50 / 200 → Informes → Balances → Sumas y saldos → Exportar CSV
  - Holded → Contabilidad → Informes → Sumas y saldos → Descargar
  - SAP B1 → Finanzas → Informes financieros → Contabilidad → Balance de comprobación
  - Odoo → Contabilidad → Informes → Balance general / Sumas y saldos
  - ContaSOL / ContaPlus → Informes → Balances → Sumas y saldos

- **Movimientos bancarios** (CSV):
  - Descárgalo directamente del portal del banco (Santander, BBVA, Caixa, Sabadell, Bankinter, etc. — todos permiten exportar CSV del extracto).
  - O si tu ERP tiene conciliación bancaria, exporta desde ahí.

Asegúrate de que las columnas coinciden con las de los CSVs de ejemplo. Si no, abre el CSV en Excel, renombra las cabeceras y guarda.

## Nota importante — sector

Este prompt está calibrado para **PYMEs industriales españolas** (fabricación, metalurgia, transformación, mecanizados) de 1 a 50M€. Los umbrales de los ratios (endeudamiento < 3,5x, liquidez > 1,2, etc.) son los que miran los analistas de riesgos para este sector.

Si tu empresa es de otro sector (hostelería, construcción, servicios profesionales, retail), ajusta los umbrales dentro del prompt antes de ejecutarlo — o pídeselo a Claude Code en el mismo chat, él los recalibra sobre la marcha.

## Qué NO hace este pack

- No sustituye a tu asesor fiscal ni a tu auditor.
- No presenta cuentas en el Registro Mercantil (eso tiene su propio proceso).
- No es un informe oficial — es un dossier interno **para negociar con el banco**.

---

Creado por Isaac Romà · https://isaacroma.com

→ Reunión gratuita de 30 min: https://calendly.com/asesor-online-ia/30min
