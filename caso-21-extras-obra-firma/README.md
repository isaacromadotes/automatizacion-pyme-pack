# Caso 21 · Extras de obra con firma digital — Deja de perder 8-25K€/año en acuerdos de palabra

> Una obra media pierde entre **8.000 € y 25.000 € al año** en extras acordados de palabra que el cliente luego no reconoce. **Sin firma, no se ejecuta.**

## 🎯 Problema que resuelve

En construcción, el ciclo del extra siempre es el mismo: el cliente llega a obra, pide un cambio de material, un tabique nuevo, un punto de luz, un refuerzo tras cata, y el jefe de obra dice "sí, lo hacemos" apretándose la mano. Dos meses después, cuando aparece la factura, el cliente responde "yo no aprobé eso" y el extra se come el margen de la obra. Multiplicado por una cartera de 5-10 obras activas y 10-15 extras por obra, son fácilmente 8.000-25.000 € al año regalados por no tener firma. El problema no es técnico, es de proceso: el jefe de obra no tiene herramienta para dejar constancia desde el móvil en el momento, los extras se apuntan en una libreta o en un WhatsApp que luego nadie reconstruye, y cuando administración los repasa dos meses después ya no hay forma de reclamar porque falta la aprobación formal. Este pack entrega el circuito completo cerrado: el jefe de obra registra el extra desde el móvil con descripción, medición, fotos y urgencia; Claude Code valora automáticamente aplicando los precios unitarios del contrato original; se emite un documento de aprobación con firma digital que llega al cliente; sin firma el extra no se ejecuta y queda en estado "pendiente" en el dashboard. Todo se consolida por obra con el acumulado aprobado, pendiente y rechazado, de modo que la dirección ve en tiempo real cuánto extra lleva vivo cada proyecto y cuánto está en riesgo de no cobrarse.

## 📦 Archivos del pack

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Documento inicial con la explicación del caso. |
| `prompt.txt` | Prompt listo para pegar en Claude Code. |
| `precios_contrato.csv` | 20 unidades de obra con precios unitarios del contrato original (albañilería, electricidad, fontanería, pintura, carpintería, climatización, impermeabilización, estructura, seguridad). |
| `extras_obra_mirador.csv` | 14 extras reales de la obra "Residencial Mirador" con fechas, mediciones, estados (aprobado/pendiente/rechazado) e importes. |
| `obras_activas.csv` | 5 obras activas de una constructora con presupuesto original y extras acumulados por estado. |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la [documentación oficial](https://docs.anthropic.com/en/docs/claude-code): `npm install -g @anthropic-ai/claude-code`
2. **Descomprime este pack** en una carpeta local (ej. `C:\Caso_21_Extras\`) y abre la terminal dentro con el comando `claude`.
3. **Arrastra a la ventana de Claude Code** el `LEEME.md`, el `prompt.txt` y los 3 CSV para que tenga todo el contexto.
4. **Copia el contenido de `prompt.txt`**, pégalo en Claude Code y sustituye `[EMPRESA]`, `[MES AÑO]` y `@ruta/` por tus datos reales.
5. **Pulsa Enter**: Claude Code genera el sistema completo (registro móvil, valoración automática, documento de firma, dashboard por obra) y arranca el servidor local para abrirlo en el navegador.

## 🔌 Cómo exportar los datos desde tu ERP

| Dato | Presto | Arquímedes / CYPE | Menfis | SAP PS | Sage 200 Construcción | A3ERP / Holded / Odoo |
|---|---|---|---|---|---|---|
| Precios unitarios de contrato | Archivo → Exportar → Excel (código, resumen, precio, ud) | Listados → Exportar mediciones y presupuesto | Utilidades → Exportar a Excel | Transacción CJ20N → Exportar estructura | Informes de presupuesto por partida | Módulo Proyectos / Fichas de artículos |
| Extras acumulados por obra | Parte diario de obra / Hoja paralela | Modificaciones de proyecto → Exportar | Partes de obra → Exportar | Modificaciones de WBS → Exportar | Partes de obra → Exportar | Partes de obra / Albaranes → Exportar |
| Obras activas con presupuesto | Lista de obras → Exportar | Proyectos activos → Exportar | Obras → Exportar | Proyectos activos CJ03 | Obras → Listado → Exportar | Proyectos / Clientes → Exportar |

> ⚠️ **Nota de sector:** este pack está diseñado para **construcción (obra nueva y reforma)**, pero el flujo "trabajo adicional de palabra → presupuesto → firma → facturación" se adapta a talleres mecánicos (reparaciones adicionales), servicios técnicos e instalaciones (correctivos), consultoría por horas (ampliación de alcance) y estudios de arquitectura o ingeniería (modificaciones de proyecto). Para cerrar el ciclo económico de la obra, combina con el [caso-03 (control de obra)](../caso-03-control-obra/), el [caso-09 (partes de obra)](../caso-09-partes-obra/), el [caso-12 (desviaciones de proyectos)](../caso-12-desviaciones-proyectos/) y el [caso-15 (certificaciones)](../caso-15-certificaciones-obra/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años en C-Suite.
Ayudo a **PYMEs industriales, mayoristas y de construcción (1-50M€)** a automatizar operaciones y recuperar margen con IA aplicada al negocio real, no a la tecnología.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min conmigo:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>extras obra no cobrados constructora, firma digital extras construcción, aprobación modificaciones obra móvil, presupuesto adicional obra automático, control extras obra jefe de obra, recuperar margen extras construcción, dashboard extras acumulados obra, flujo aprobación modificaciones proyecto, acuerdos de palabra en obra cobrar, software extras obra pyme construcción</sub>
