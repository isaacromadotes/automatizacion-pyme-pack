# Caso 54 — Cobros se retrasan sin seguimiento sistemático

## El problema que resuelve

Tu empresa factura bien pero cobra tarde. Nadie persigue las facturas vencidas de forma sistemática. El DSO (días medios de cobro) sube de 45 a 70, 90, 120 días. La tesorería sufre, pides pólizas de crédito, pagas intereses, y encima tienes clientes que llevan meses sin pagar y nadie les ha reclamado.

**Dolor real:** Un consultora de 2M€ facturación con DSO de 70 días tiene 390.000€ atrapados en cuentas a cobrar. Reducir el DSO en 15 días = **83.000€ liberados en caja** sin vender ni un euro más.

Este pack te genera el sistema completo de seguimiento automático: aging de facturas, dashboard DSO con semáforos, 3 emails de reclamación escalonados (cordial → firme → ultimátum) y una regla de bloqueo automático de servicio para los morosos crónicos.

## Qué contiene este ZIP

- `LEEME.md` — este archivo
- `prompt.txt` — prompt completo para pegar en Claude Code
- `facturas_pendientes.csv` — ejemplo con 12 facturas de clientes variados
- `historial_pagos.csv` — DSO real medio histórico por cliente
- `diseno.txt` — guía de estilo visual para el panel HTML

## Cómo usarlo paso a paso

1. **Instala Claude Code** (si no lo tienes):
   - Ve a https://claude.com/claude-code y sigue las instrucciones de instalación.
   - Necesitas una cuenta de Anthropic con plan Pro o superior.

2. **Prepara los archivos de este ZIP:**
   - Descomprime el ZIP en una carpeta de tu equipo (ejemplo: `C:\CobrosClaude\` o `~/CobrosClaude/`).
   - Dentro verás los 5 archivos listados arriba.

3. **Sustituye los CSVs de ejemplo por los tuyos:**
   - Exporta tu aging de facturas y tu histórico de pagos desde tu ERP (ver sección de abajo).
   - Mantén los **mismos nombres de columna** que los CSVs de ejemplo.
   - Guarda los archivos en la misma carpeta, con los mismos nombres.

4. **Abre Claude Code:**
   - Abre tu terminal (iTerm en Mac, PowerShell en Windows).
   - Navega a la carpeta: `cd ~/CobrosClaude/`
   - Escribe `claude` y pulsa Enter.

5. **Pega el prompt:**
   - Abre `prompt.txt`, copia todo el contenido.
   - Antes de pegar, cambia estas variables:
     - `[EMPRESA]` → el nombre de tu empresa
     - `[MES AÑO]` → el mes de análisis (ej. "Octubre 2026")
     - `@ruta/` → la ruta absoluta de tu carpeta
   - Pega en Claude Code y pulsa Enter.

6. **Espera el resultado:**
   - Claude Code analizará los CSVs, calculará aging y DSO, generará el panel web y lo arrancará automáticamente.
   - También generará un Excel con los emails, la regla de bloqueo y un PDF de proyección.

## De dónde sacar los datos en tu ERP

| ERP | Ruta de exportación |
|-----|---------------------|
| **A3 ERP** | Ventas → Facturas → Pendientes de cobro → Exportar a Excel |
| **Sage 50/200** | Ventas → Cartera de efectos → Pendientes → Exportar CSV |
| **Holded** | Facturación → Facturas de venta → Filtro "Pendiente" → Exportar |
| **SAP Business One** | Business Partners → Cuentas por cobrar → Aging report |
| **Odoo** | Contabilidad → Clientes → Facturas → Filtros: No pagadas |
| **Contasol** | Procesos → Cartera → Vencimientos pendientes |

Asegúrate de que tu export incluye: cliente, nº factura, importe, fecha emisión, fecha vencimiento, email de contacto.

Para el histórico de DSO: la mayoría de ERPs tienen un informe "Días medios de cobro por cliente" en el módulo de analítica. Si no, calcúlalo con una fórmula simple: (días desde emisión hasta cobro) / número de facturas cobradas.

## ⚠️ Nota importante

Este prompt está diseñado para **PYMEs de servicios** (consultoría, asesoría, agencias, SaaS B2B) con ciclo de cobro a 30/60/90 días. Si tu sector es:

- **Construcción:** aumenta los umbrales a 60/90/120 días (los pagos suelen ir a certificaciones).
- **Comercio minorista:** probablemente no te sirve este prompt (cobras al contado).
- **Industria/distribución:** mantén los umbrales pero añade descuentos por pronto pago en la lógica.

## Firma

Creado por Isaac Romà · https://isaacroma.com
