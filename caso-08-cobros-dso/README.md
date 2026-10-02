# Caso 08 · Sistema de cobros y reducción de DSO — Libera cientos de miles de euros de liquidez

> **Resultado clave:** Automatiza el ciclo de cobros, reduce el DSO de 78 a 54 días y libera +450.000€ de liquidez inmediata en una empresa de 7M€ de facturación. Reclamaciones escalonadas, bloqueo automático de pedidos a morosos y dashboard de riesgo en tiempo real.

## 🎯 Problema que resuelve

En la mayoría de PYMEs mayoristas y de distribución españolas los cobros se gestionan de forma manual y reactiva: alguien revisa las facturas vencidas en el ERP cuando tiene tiempo, envía recordatorios sin un criterio claro, y los nuevos pedidos siguen entrando aunque el cliente arrastre deuda antigua. El resultado es un DSO (Days Sales Outstanding) disparado — habitualmente entre 75 y 90 días en el sector — que atrapa cientos de miles de euros en cuentas por cobrar y obliga a la empresa a financiarse con póliza para pagar nóminas y proveedores. Peor aún: el equipo comercial no tiene visibilidad del riesgo cliente, el financiero no tiene criterios automáticos de bloqueo, y las reclamaciones se envían tarde, mal o nunca. Este caso automatiza el ciclo completo: cálculo del DSO real, clasificación de deuda por antigüedad (0-30, 31-60, 61-90, +90), generación de emails de reclamación escalonados por tramo, reglas automáticas de bloqueo de pedidos por límite de crédito y antigüedad de deuda, y dashboard interactivo de riesgo cliente. Pensado para PYMEs mayoristas de 1-50M€ donde reducir 20-25 días de DSO puede liberar entre 300.000€ y 1,5M€ de caja.

## 📦 Archivos del pack

| Archivo | Descripción |
|---------|-------------|
| `LEEME.md` | Instrucciones de uso del caso |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `facturas_emitidas.csv` | 127 facturas de ejemplo de "Suministros Levante S.L." |
| `maestro_clientes.csv` | 15 clientes con contacto, condiciones de pago y límite de crédito |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** si aún no lo tienes: `npm install -g @anthropic-ai/claude-code` (requiere Node.js 18+ y cuenta Anthropic con API key). Guía oficial: [docs.anthropic.com/en/docs/claude-code](https://docs.anthropic.com/en/docs/claude-code)
2. **Copia los 2 CSVs** del pack a una carpeta de tu ordenador (ej: `C:\Users\TU_USUARIO\Downloads\Cobros\`). Si quieres probar con datos reales, sustituye los archivos manteniendo las mismas columnas.
3. **Abre tu terminal** (CMD, PowerShell o Terminal en Mac) y lanza `claude` desde la carpeta donde están los archivos.
4. **Pega el `prompt.txt`** y antes de pulsar Enter sustituye las variables: `[EMPRESA]` por el nombre de tu empresa, `[MES AÑO]` por el período a analizar y `@ruta/` por la ruta real de tus CSVs.
5. **Pulsa Enter y espera**. Claude Code calcula el DSO, clasifica la deuda por antigüedad, genera emails de reclamación escalonados, aplica reglas de bloqueo y entrega un dashboard HTML interactivo + Excel + PDF ejecutivo.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Facturas emitidas | Maestro clientes |
|-----|-------------------|------------------|
| **A3 (a3ERP / a3innuva)** | Contabilidad → Cuentas a cobrar → Exportar facturas emitidas (CSV/Excel) | Maestro de clientes → Exportar |
| **Sage 200** | Informes → Cartera de efectos / Antigüedad saldos → Exportar Excel | Clientes → Ficha → Exportar listado |
| **Holded** | Ventas → Facturas → Exportar CSV | Contactos → Exportar clientes |
| **SAP Business One** | Finanzas → Informe antigüedad de deuda → Exportar | Socios de negocio → Exportar maestro |
| **Odoo** | Contabilidad → Informes → Antigüedad cuentas por cobrar → XLSX | Contactos → Exportar clientes |
| **Contasol / ContaPlus** | Informes → Mayor de clientes / Antigüedad saldos → Exportar | Maestro de clientes → Listado |

⚠️ **Nota de sector:** Este caso está optimizado para **empresas mayoristas y de distribución**, donde el DSO alto y la morosidad recurrente son el principal problema de caja. Funciona igual en **fabricación** (ajustando condiciones de pago habituales a 60-90 días) y en **servicios profesionales**. En **construcción**, la gestión de cobros se cruza con certificaciones de obra — en ese caso combínalo con el **Caso 15 · Certificaciones de obra**.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con 20 años en C-Suite. Ayudo a PYMEs españolas de **1-50M€** (industria, mayoristas y construcción) a automatizar procesos ejecutivos y traducir operaciones a impacto financiero real (EBITDA, caja, margen).

- **Diagnóstico inicial:** 750€
- **Automatización a medida:** desde 4.500€
- **Acompañamiento mensual:** 300€/mes

👉 **Reserva 30 min gratis:** [calendly.com/asesor-online-ia/30min](https://calendly.com/asesor-online-ia/30min)

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>reducir DSO PYME, sistema cobros automatizado, morosidad clientes mayorista, liberar liquidez cuentas por cobrar, automatización financiera PYME, dashboard riesgo cliente, Claude Code España, consultor IA PYME, antigüedad deuda clientes, bloqueo automático pedidos morosos</sub>
