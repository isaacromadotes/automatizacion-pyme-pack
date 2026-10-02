# Caso 45 · Licitaciones de obra pública — Rastreo semanal filtrado por CNAE, zona e importe

> **Resultado:** De 3 ofertas al mes vistas por casualidad a 12 licitaciones encajadas con antelación. HTML visual con las 5 más urgentes + Excel con el total del mes filtrado + email semanal listo para enviar al equipo comercial.

## 🎯 Problema que resuelve

Para una PYME constructora que depende total o parcialmente de obra pública, cada licitación que no ve a tiempo es dinero que pierde sin posibilidad de recuperarlo. El sistema actual en la mayoría de constructoras pequeñas y medianas españolas es puramente oportunista: un comercial avisa de un concurso que escuchó, un conocido lo menciona en una reunión del sector, el jefe de obra se entera porque se publica tarde en un boletín autonómico que nadie leyó. Resultado: la empresa presenta 3 ofertas al mes cuando el mercado estaba publicando 20 o 30 encajadas con su CNAE, su clasificación de contratista y su zona geográfica, y las pocas que presenta las prepara con prisas porque llegaron a dos semanas del cierre, con poco margen para visitar la obra, cuadrar precios con proveedores o estudiar la memoria técnica con calma. El problema no es la falta de obra pública —el volumen licitado en España supera año tras año los 25-30 mil millones— sino la fragmentación de fuentes (PLACSP, DOGV, BOCA, BOCM, perfiles de contratante de cientos de ayuntamientos y diputaciones) y la ausencia de un filtrado disciplinado por los criterios reales de la empresa: código CNAE, clasificación de contratista, importe de licitación compatible con avales, zona geográfica razonable, tipo de obra que la empresa sabe ejecutar bien. Este caso automatiza el rastreo semanal, aplica los filtros por CNAE / zona / importe / tipo de obra y entrega tres salidas: HTML visual con las 5 licitaciones que más encajan ordenadas por plazo urgente, Excel con el total del mes filtrado y email semanal listo para enviar al equipo comercial con las acciones a priorizar.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `criterios_busqueda.csv` | Criterios de filtrado (CNAE, zona, importe, tipo de obra) |
| `licitaciones_ejemplo.csv` | Simulación de 12 licitaciones publicadas en un mes |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_45_Licitaciones\`) con los 2 CSVs en la raíz.
3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md`, `prompt.txt` y los 2 CSVs** al chat para dar contexto antes de ejecutar.
5. **Edita `prompt.txt`** cambiando `[EMPRESA]` y `[MES AÑO]`, pégalo y pulsa Enter. Obtendrás HTML visual + Excel filtrado + email semanal listo para enviar al equipo comercial.

## 🔌 Cómo exportar los datos desde fuentes públicas y ERP

| Fuente | Qué obtienes | Dónde |
|---|---|---|
| **PLACSP (Plataforma Contratación Sector Público)** | XML/CSV diario de todas las licitaciones estatales | contrataciondelestado.es → Descargas |
| **DOGV / BOCA / BOCM / DOGC / BOPV / DOG...** | Licitaciones autonómicas | Boletín oficial de cada comunidad |
| **Perfil del contratante (ayuntamientos y diputaciones)** | Licitaciones locales | Web del organismo contratante |
| **Insight View / Vortal / Licitia / Einforma** | Agregadores de licitaciones de pago | Suscripción |
| **CYPE / Presto** | Base de precios para preparar oferta | Módulo mediciones y presupuestos |
| **Menfis** | Estudio de licitación y seguimiento | Módulo licitaciones |
| **A3 Innuva / Sage 200 Construcción** | Clasificación contratista, histórico adjudicaciones | Módulo obras |
| **Holded / Odoo** | Pipeline comercial de licitaciones | CRM / Proyectos |

Lo ideal es que un script o un servicio automatizado descargue cada noche los nuevos pliegos de PLACSP y de los boletines autonómicos relevantes y los guarde como CSV diario. Es un montaje que se hace una vez y queda operativo.

> ⚠️ **Nota de sector:** Diseñado para **empresas de construcción, obra civil, rehabilitación y edificación** (CNAE 41-43) que operan con obra pública. Para **suministros al sector público** (material sanitario, mobiliario, informática, material de oficina) cambia los criterios del CSV por categoría de suministro y lotes. Para **servicios al sector público** (consultoría, formación, asistencia técnica) adapta tipo de contrato (servicios en vez de obras) y pliegos técnicos. La lógica del prompt es la misma. Para enlazar con la gestión de la obra adjudicada, combina con [caso-33 (reporting trimestral socios y banco)](../caso-33-reporting-trimestral-socios-banco/) y [caso-39 (posición financiera por obra)](../caso-39-posicion-financiera-por-obra/).

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>licitaciones obra pública PYME constructora, rastreo PLACSP automatizado, filtrado CNAE zona importe licitación, Claude Code licitaciones públicas, DOGV BOCA BOCM perfil contratante, clasificación contratista constructora, pipeline comercial obra pública, agregadores Insight View Vortal, automatización comercial construcción, consultoría automatización obra pública PYME España</sub>
