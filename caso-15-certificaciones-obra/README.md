# Caso 15 · Certificaciones de obra sin retraso — Cobra 10 días antes cada mes

> En una obra de **6M€**, adelantar la certificación mensual **10 días** mete **150–200K€ antes en caja**.

## 🎯 Problema que resuelve

En construcción, certificar tarde es cobrar tarde: la mayoría de constructoras pequeñas y medianas certifican entre el día 5 y el 15 del mes siguiente porque el jefe de obra tiene que cruzar partes a mano, cuadrar con la certificación acumulada anterior y montar el PDF para firma. Son 7-10 días de trabajo manual que podrían estar siendo liquidez. En una obra de 6M€ con certificación mensual del 8-10%, cada día que se retrasa la firma son entre 15.000 € y 20.000 € parados en el circuito administrativo mientras tu banco cobra pólizas y tus subcontratas te presionan para que les pagues. El problema no es la obra, es el proceso: cruzar el libro de partes del mes con la certificación anterior, aplicar precios unitarios por capítulo, calcular acumulados, detectar desviaciones sobre presupuesto y montar un documento firmable es trabajo repetitivo que se hace una vez al mes y siempre tarde. Este pack automatiza el ciclo completo: Claude Code lee los partes validados y la certificación anterior, calcula la certificación del mes por capítulos con acumulados, genera el PDF listo para firma digital, el Excel de soporte con KPIs de obra y un informe HTML ejecutivo para la dirección. El día 1 del mes todo está sobre la mesa.

## 📦 Archivos del pack

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Documento inicial con la explicación del caso. |
| `prompt.txt` | Prompt listo para pegar en Claude Code. |
| `partes_obra.csv` | Partes validados del mes (datos ficticios de demo). |
| `certificaciones_anteriores.csv` | Acumulado certificado hasta la fecha. |
| `instrucciones_para_crear_tabla_excel.txt` | Guía de estilo visual del Excel de soporte (paleta, layout, KPIs, tipografía). |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la [documentación oficial](https://docs.anthropic.com/en/docs/claude-code): `npm install -g @anthropic-ai/claude-code`
2. **Descomprime este pack** en una carpeta local (ej. `C:\Certificaciones\Obra_XX\`) y abre la terminal dentro con el comando `claude`.
3. **Arrastra a la ventana de Claude Code** el `LEEME.md`, el `prompt.txt`, los 2 CSV y el `instrucciones_para_crear_tabla_excel.txt`.
4. **Copia el contenido de `prompt.txt`**, pégalo en Claude Code y sustituye `[EMPRESA]`, `[OBRA]` y `[MES AÑO]` por tus datos.
5. **Pulsa Enter**: Claude Code valida los partes, cruza con la certificación anterior, calcula acumulados por capítulo y genera el PDF firmable, el Excel de soporte y el informe HTML ejecutivo en la misma carpeta.

## 🔌 Cómo exportar los datos desde tu ERP

| Dato | A3ERP / A3CON | Sage 50/200 Construcción | Presto | Menfis / Arquímedes | Odoo Construction | SAP S/4HANA |
|---|---|---|---|---|---|---|
| Partes de obra del mes | Obras → Partes de trabajo → Exportar CSV | Obras → Partes → Exportar | Partes de obra → Exportar | Partes → Exportar Excel | Proyectos → Partes de obra → Exportar CSV | Transacción CJ74 → Exportar |
| Certificaciones anteriores | Obras → Certificaciones → Exportar | Obras → Certificaciones → Exportar libro Excel | Certificación en formato BC3 o Excel | Certificaciones → Exportar Excel | Proyectos → Certificaciones → Exportar | Transacción CN41 → Exportar |

> ⚠️ **Nota de sector:** este pack está diseñado específicamente para **construcción y promoción inmobiliaria** (constructoras, promotoras, subcontratas). La lógica de certificación por capítulos, precios unitarios y acumulados es propia del sector. Para control económico más fino del ciclo de obra, encadena con el [caso-03 (control de obra en tiempo real)](../caso-03-control-obra/), el [caso-09 (partes de obra)](../caso-09-partes-obra/) y el [caso-12 (desviaciones de proyectos)](../caso-12-desviaciones-proyectos/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años en C-Suite.
Ayudo a **PYMEs industriales, mayoristas y de construcción (1-50M€)** a automatizar operaciones y recuperar margen con IA aplicada al negocio real, no a la tecnología.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **Automatización a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min conmigo:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>certificación mensual obra automática, certificaciones construcción sin retraso, automatizar certificaciones constructora, pdf certificación obra firma digital, cobrar antes certificación obra, acumulado certificación por capítulos, partes de obra a certificación automática, software certificaciones obra pyme, reducir dso constructora, flujo de caja obra construcción</sub>
