# Caso 41 — Auditoría IFS v8 en 1 hora en vez de 2 semanas

## El problema

Tienes la auditoría de IFS en 3 semanas. Tus registros APPCC no están al día. Siempre es lo mismo: **2 semanas de estrés** preparando documentación, cruzando temperaturas, limpiezas, formación y no conformidades a mano.

Este pack convierte ese caos en un **dossier de auditoría estructurado por capítulos IFS v8** y un **check-list Excel de 47 puntos** (OK / Pendiente) en menos de 1 hora.

## Qué contiene este ZIP

- `LEEME.md` — este archivo
- `prompt.txt` — el prompt que pegarás en Claude Code
- `registros_appcc.csv` — puntos de control críticos (temperaturas, pH, detector de metales, esterilización...)
- `limpiezas.csv` — plan de L+D por zona y responsable
- `formacion.csv` — formación obligatoria del personal (manipulación, APPCC, alérgenos...)
- `no_conformidades.csv` — NC detectadas, acción correctiva, estado y evidencia

## Cómo usarlo paso a paso

1. **Instala Claude Code** → https://claude.com/claude-code
2. **Crea una carpeta** en tu equipo (ej: `C:\Auditoria_IFS\`) y copia dentro los 4 CSV
3. **Abre Claude Code** desde la terminal en esa carpeta
4. **Arrastra el `LEEME.md` y el `prompt.txt`** a la ventana de Claude Code para que entienda el contexto antes de ejecutar
5. **Abre `prompt.txt`**, cambia las variables entre corchetes:
   - `[EMPRESA]` → nombre real de tu empresa
   - `[MES AÑO]` → ej: septiembre 2026
   - `@ruta/` → ruta donde tienes los CSV
6. **Pega el prompt** en Claude Code y pulsa Enter
7. Al terminar tendrás en la misma carpeta: **dossier HTML** navegable por capítulos IFS v8 + **check-list Excel** con los 47 puntos marcados

## De dónde sacar los datos reales en tu empresa

- **Registros APPCC** → tu software de calidad (Isotools, Kaizen Compliance, Calidadlive, QGEST), hojas de ruta en producción, dataloggers de temperatura
- **Limpiezas** → partes de limpieza del encargado de calidad, planning L+D firmado
- **Formación** → RRHH, A3 Nom / Sage / Factorial / Personio — exporta "cursos realizados por empleado"
- **No conformidades** → módulo de NC de tu ERP de calidad o Excel maestro de NC

Si tus datos están en PDF o papel firmado, escanéalos y conviértelos a CSV antes (o pide a tu asesor que te lo exporte).

## ⚠️ Importante — Sector específico

Este prompt está diseñado para **PYMEs agroalimentarias** que se auditan bajo **IFS Food v8**. Si tu norma de referencia es **BRCGS, FSSC 22000, ISO 22000 o IFS Logistics**, cambia la referencia en el prompt — Claude Code adapta la estructura del dossier a la norma que indiques.

Los puntos del check-list cubren los 10 capítulos principales de IFS Food v8:
1. Responsabilidad de la dirección
2. Sistema de gestión de la calidad y seguridad alimentaria
3. Gestión de recursos
4. Procesos operativos
5. Mediciones, análisis y mejoras
6. Food Defense

---

Creado por Isaac Romà · https://isaacroma.com
