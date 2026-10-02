# INSTRUCCIONES PARA LA WEB / BLOG

**Bloque de instrucciones para publicar junto a la descarga del ZIP:**

---

### Cómo usar este pack

1. **Descarga el ZIP y descomprímelo** en una carpeta de tu equipo (por ejemplo `C:\Mantenimiento\` o `~/Mantenimiento/`).

2. **Instala Claude Code** si aún no lo tienes: https://claude.ai/code

3. **Abre tu terminal** (CMD o PowerShell en Windows, Terminal en Mac) y escribe:
   ```
   claude
   ```

4. **Importante — arrastra el contexto primero**: antes de pegar nada, arrastra el `LEEME.md` y el `prompt.txt` dentro de la ventana de Claude Code. Esto hace que la IA entienda el contexto completo del caso (el problema, los datos, el objetivo) antes de ejecutar nada.

5. **Pega el contenido del `prompt.txt`** en Claude Code.

6. **Cambia las variables** marcadas con corchetes:
   - `[EMPRESA]` → el nombre de tu empresa
   - `[MES AÑO]` → el periodo analizado (ej. "Octubre 2026")
   - `@ruta/` → la ruta donde tienes los CSV

7. **Pulsa Enter** y espera. Claude Code analiza el histórico, detecta patrones cíclicos, calcula el payback de cada acción y genera 3 entregables: Excel con el plan completo, dashboard HTML para el gerente y PDF ejecutivo para dirección.

Si quieres probarlo con tus datos reales, exporta el histórico de paros y el catálogo de máquinas de tu GMAO (Prisma, SAP PM, Fracttal, Mecalux) en CSV y sustituye los de ejemplo. El `LEEME.md` incluye la ruta exacta de exportación para cada GMAO.
