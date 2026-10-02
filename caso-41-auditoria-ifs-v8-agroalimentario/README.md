# Caso 41 · Auditoría IFS v8 en 1 hora en vez de 2 semanas — Dossier estructurado + check-list de 47 puntos

> **Resultado:** De 2 semanas de estrés preparando documentación APPCC a 1 hora. Dossier HTML navegable por capítulos IFS Food v8 + check-list Excel de 47 puntos (OK / Pendiente) listo para el auditor.

## 🎯 Problema que resuelve

En toda PYME agroalimentaria que trabaja con gran distribución la auditoría IFS Food v8 se vive cada año como una tormenta previsible: llega el aviso con 3 semanas de margen y empiezan las dos semanas de pánico donde el responsable de calidad abandona todo lo demás para cruzar a mano registros APPCC dispersos en dataloggers, hojas de ruta de producción, partes de limpieza firmados en papel, cursos de formación en nóminas y acciones correctivas que llevan meses abiertas sin cerrar. El problema no es que la empresa trabaje mal —muchas cumplen los puntos de control en su día a día— sino que la evidencia documental está fragmentada entre media docena de sistemas (software de calidad tipo Isotools o QGEST, dataloggers, Excel de L+D, Factorial o Sage Nom para formación, módulo de NC o Excel maestro) y nadie puede componer en tiempo real la narrativa que un auditor espera: capítulo por capítulo, con trazabilidad y evidencia asociada. El coste real son dos semanas del responsable de calidad y del gerente perdidas en reporting en lugar de en mejora continua, horas extra del equipo, nervios en jornada de auditoría y, cuando sale mal, no conformidades que podrían haberse detectado y cerrado con antelación. Este caso automatiza el cruce de registros APPCC, planes de limpieza, formación obligatoria y no conformidades, genera un dossier HTML navegable organizado por los capítulos oficiales de IFS Food v8 con evidencia por punto y un check-list Excel de 47 puntos (OK / Pendiente / Evidencia faltante) listo para repasar con el equipo antes del día de la auditoría.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `registros_appcc.csv` | Puntos de control críticos (temperaturas, pH, detector de metales, esterilización) |
| `limpiezas.csv` | Plan de L+D por zona y responsable |
| `formacion.csv` | Formación obligatoria del personal (manipulación, APPCC, alérgenos) |
| `no_conformidades.csv` | NC detectadas, acción correctiva, estado y evidencia |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_41_Auditoria_IFS\`) con los 4 CSVs en la raíz.
3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md`, `prompt.txt` y los 4 CSVs** al chat para dar contexto antes de ejecutar.
5. **Edita `prompt.txt`** cambiando `[EMPRESA]`, `[MES AÑO]` y `@ruta/`, pégalo y pulsa Enter. Obtendrás dossier HTML navegable por capítulos IFS v8 + check-list Excel con 47 puntos.

## 🔌 Cómo exportar los datos desde tu software

| Software / Fuente | Registros APPCC | Limpiezas (L+D) | Formación | No conformidades |
|---|---|---|---|---|
| **Isotools** | PCC → Export registros | Plan limpieza → Export | Formación → Cursos realizados | Módulo NC → Export |
| **Kaizen Compliance** | APPCC → Registros digitales | Planning L+D | Formación | NC + acciones correctivas |
| **Calidadlive** | Registros PCC | Partes limpieza | Formación personal | NC → Estado y evidencia |
| **QGEST** | Puntos de control | Plan L+D firmado | Matriz formación | Módulo NC |
| **Dataloggers (Testo, Kimo, Ebro)** | Temperaturas → Export CSV | — | — | — |
| **A3 Nom / Sage Nom / Factorial / Personio** | — | — | Cursos realizados por empleado | — |
| **Excel maestro / papel escaneado** | OCR a CSV con 6 columnas base | Partes firmados → Excel | Registro de formación anual | Excel maestro NC |

Si tus datos están en PDF firmados o en papel, escanea y convierte a CSV antes de pasarlo a Claude Code (o pide a tu asesor de calidad que exporte).

> ⚠️ **Nota de sector:** Diseñado para **PYMEs agroalimentarias auditadas bajo IFS Food v8**. Si tu norma de referencia es **BRCGS, FSSC 22000, ISO 22000, IFS Logistics, IFS Broker o Global G.A.P.**, cambia la referencia en el prompt y Claude Code adaptará la estructura del dossier a la norma indicada (manteniendo evidencias y check-list). Para enlazar el cumplimiento con el coste real del producto certificado, combina con [caso-29 (coste real por referencia en gran distribución)](../caso-29-coste-real-gran-distribucion/); para anticipar impacto de campaña y auditoría sobre la caja, con [caso-35 (estacionalidad tesorería agroalimentario)](../caso-35-estacionalidad-tesoreria-agroalimentario/).

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>auditoría IFS Food v8 PYME, preparación dossier IFS automatizada, APPCC registros temperatura pH, Claude Code calidad agroalimentaria, check-list IFS 47 puntos, BRCGS FSSC 22000 ISO 22000, no conformidades acción correctiva, formación APPCC alérgenos manipulación, dataloggers Isotools QGEST, consultoría automatización calidad agroalimentaria España</sub>
