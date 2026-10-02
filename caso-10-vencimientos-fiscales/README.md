# Caso 10 · Vencimientos fiscales controlados — Cero sanciones y adiós al modo bombero trimestral

> **Resultado clave:** Cruza automáticamente tu cartera de clientes con el calendario de la AEAT, calcula todos los vencimientos del mes, genera emails de aviso al gestor y al cliente, y lo entrega en un dashboard con semáforo de urgencias. Ahorra 15-25 horas al trimestre y elimina sanciones por plazos escapados.

## 🎯 Problema que resuelve

Las gestorías y asesorías fiscales españolas con 200-500 clientes gestionan los vencimientos tributarios con agenda de papel, un Excel manual que nadie actualiza o directamente de memoria. El resultado se repite cada trimestre: plazos que se escapan, modelos presentados fuera de tiempo, sanciones de la AEAT que el despacho acaba comiéndose para no perder al cliente, y un equipo viviendo en modo bombero las dos semanas previas al 20 de cada mes. El problema de fondo es que nadie cruza de forma sistemática el régimen fiscal específico de cada cliente (IVA general, recargo de equivalencia, módulos, SII, grupo IVA, Sociedades, retenciones) con el calendario oficial de la AEAT, así que las obligaciones se detectan a mano, cliente a cliente, con el consiguiente riesgo de olvido. Este caso automatiza el proceso completo: cruce clientes × obligaciones por régimen fiscal, cálculo de todos los vencimientos del mes/trimestre, generación automática de emails escalonados (al gestor interno y al cliente), dashboard HTML interactivo con filtros por gestor y modelo, y semáforo de urgencia (verde >15 días, ámbar 5-15 días, rojo <5 días). Pensado para asesorías y despachos profesionales que facturan entre 300.000€ y 5M€ y cuya rentabilidad depende de la productividad por gestor.

## 📦 Archivos del pack

| Archivo | Descripción |
|---------|-------------|
| `LEEME.md` | Instrucciones de uso del caso |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `clientes_fiscal.csv` | 50 clientes de ejemplo con CIF, gestor, régimen IVA y tipo de sociedad |
| `calendario_fiscal.csv` | Calendario AEAT con modelos, plazos y aplicabilidad por régimen |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** si aún no lo tienes: `npm install -g @anthropic-ai/claude-code` (requiere Node.js 18+ y cuenta Anthropic con API key). Guía oficial: [docs.anthropic.com/en/docs/claude-code](https://docs.anthropic.com/en/docs/claude-code)
2. **Copia los 2 CSVs** del pack a una carpeta de tu ordenador (ej: `C:\Users\TU_USUARIO\Downloads\Fiscal\`).
3. **Abre tu terminal** (CMD, PowerShell o Terminal en Mac) y lanza `claude` desde la carpeta donde están los archivos.
4. **Pega el `prompt.txt`** y antes de pulsar Enter sustituye las variables: `[EMPRESA]` por el nombre de tu asesoría, `[MES AÑO]` por el período a controlar (ej. "Julio 2025") y `@ruta/` por la ruta real de tus CSVs.
5. **Pulsa Enter y espera**. Claude Code valida los datos, cruza clientes × obligaciones, calcula los vencimientos del mes, genera los emails de aviso y abre un dashboard HTML profesional en tu navegador.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Clientes fiscal | Calendario fiscal |
|-----|-----------------|-------------------|
| **A3 Asesor / A3 ECO** | Ficheros → Empresas → Exportar (Datos fiscales → Régimen IVA) | Calendario del contribuyente AEAT |
| **Sage Despachos** | Listado empresas con filtro por tipo sociedad y régimen | AEAT: agenciatributaria.es (publicado cada diciembre) |
| **Holded** | Contactos → Clientes → Exportar CSV | Calendario AEAT anual |
| **SAP Business One** | Informe socios de negocio con campos fiscales | AEAT + ajuste manual por cliente |
| **Odoo** | Contactos → Exportar (fiscal_position, company_type) | Calendario AEAT importado como CSV |
| **Contasol / ContaPlus** | Maestro de empresas → Exportar con datos tributarios | AEAT: calendario oficial |

⚠️ **Nota de sector:** Este caso está diseñado para **asesorías fiscales y gestorías españolas** operando bajo el régimen común de la **AEAT**. Los modelos tributarios (303, 111, 115, 130, 200, 390, 347, 349, etc.) y plazos corresponden al calendario oficial estatal. Si tu despacho opera en **régimen foral** (País Vasco — Diputaciones de Álava, Bizkaia o Gipuzkoa — o Navarra), deberás adaptar los modelos y plazos a la Hacienda Foral correspondiente. El calendario del ZIP es de ejemplo: actualízalo al trimestre que necesites controlar.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con 20 años en C-Suite. Ayudo a PYMEs españolas de **1-50M€** (industria, mayoristas y construcción) a automatizar procesos ejecutivos y traducir operaciones a impacto financiero real (EBITDA, caja, margen).

- **Diagnóstico inicial:** 750€
- **Automatización a medida:** desde 4.500€
- **Acompañamiento mensual:** 300€/mes

👉 **Reserva 30 min gratis:** [calendly.com/asesor-online-ia/30min](https://calendly.com/asesor-online-ia/30min)

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>vencimientos fiscales asesoría, calendario AEAT automático, control plazos tributarios gestoría, automatización asesoría fiscal España, dashboard vencimientos modelos 303 111 115 130, Claude Code gestoría, consultor IA asesoría, evitar sanciones AEAT, SII vencimientos, modelo 200 Sociedades</sub>
