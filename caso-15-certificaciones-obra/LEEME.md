# Caso 15 · Certificaciones de obra sin retraso

## El problema

En construcción, certificar tarde = cobrar tarde. En una obra de 6M€, adelantar
10 días la certificación mensual pone 150–200K€ antes en caja.

La mayoría de constructoras pequeñas y medianas certifican entre el día 5 y el 15
del mes siguiente porque el jefe de obra tiene que cruzar partes a mano, cuadrar
con la certificación anterior y montar el PDF para firma. Este pack automatiza
todo ese proceso: Claude Code genera la certificación mensual completa (PDF +
Excel + informe HTML ejecutivo) el día 1 del mes, lista para firma digital.

## Qué contiene este ZIP

- `LEEME.md` — este archivo
- `prompt.txt` — el prompt a pegar en Claude Code
- `partes_obra.csv` — partes validados del mes (datos ficticios)
- `certificaciones_anteriores.csv` — acumulado certificado hasta hoy
- `instrucciones_para_crear_tabla_excel.txt` — estilo visual para el Excel
  de soporte (paleta, layout, KPIs, tipografía)

## Cómo usarlo (5 minutos)

1. Instala Claude Code si aún no lo tienes: https://claude.com/claude-code
2. Descomprime este ZIP en `~/Downloads/Ejemplo Claude Code/Vídeo 15/` (Mac)
   o `C:\Users\<tuusuario>\Downloads\Ejemplo Claude Code\Vídeo 15\` (Windows)
3. Abre tu terminal en esa carpeta y ejecuta: `claude`
4. Copia el contenido de `prompt.txt` y pégalo en Claude Code
5. Cambia las variables `[EMPRESA]`, `[OBRA]`, `[MES AÑO]` por las tuyas
6. Enter. Claude Code genera los 3 entregables en la misma carpeta

## De dónde sacar los datos en tu ERP

- **A3ERP / A3CON**: módulo Obras → Partes de trabajo → exportar a CSV
- **Sage 50 / 200 Construcción**: Obras → Certificaciones → Exportar libro Excel
- **Presto**: exportar certificación en formato BC3 o Excel
- **Menfis / Arquímedes**: Certificaciones → Exportar a Excel
- **Odoo Construction**: Proyectos → Partes de obra → Exportar CSV
- **SAP S/4HANA**: transacción CJ74 o CN41 → exportar

Si tu ERP no exporta directamente en el formato de estos CSV, pídele a Claude
Code que adapte el prompt a las columnas que sí exporta tu ERP.

## Sector

Este prompt está diseñado para **construcción y promoción inmobiliaria**
(constructoras, promotoras, subcontratas). La lógica de certificación por
capítulos, precios unitarios y acumulados es específica de este sector.

---

Creado por Isaac Romà · https://isaacroma.com
