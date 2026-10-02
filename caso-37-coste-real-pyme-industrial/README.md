# Caso 37 · Precio fijado "como siempre" sin saber el coste real — Deja de vender a pérdida en PYMEs industriales

> **Resultado:** Coste unitario real + margen por referencia + precio mínimo viable al 20% cruzando escandallos, precios de compra actualizados, tiempos de MOD e indirectos. Tabla web interactiva + Excel de escandallo + alertas PDF.

## 🎯 Problema que resuelve

En una PYME industrial o metalúrgica el gerente lleva años aplicando la misma lista de precios con subidas lineales del 2-3% anual, sin tocar la estructura de costes de fondo. Mientras tanto el acero ha subido con fuerza y volatilidad, la mano de obra ha crecido por convenio y escasez de perfiles técnicos, la luz y el gas se han disparado hasta multiplicarse en algunos períodos, y los costes indirectos (mantenimiento, calidad, logística interna, amortizaciones de maquinaria renovada) nadie los reparte bien entre referencias porque sigue vigente una regla de reparto heredada de hace una década. El resultado es un portfolio donde una parte significativa de las referencias se vende a pérdida real sin que nadie lo sepa, y los descuentos adicionales que el comercial concede a los mejores clientes salen directamente del bolsillo de la empresa. En producción se trabaja a tope, el P&L arroja beneficio contable y la caja se tensiona cada mes porque el margen bruto real es muy inferior al teórico. Este caso automatiza el cruce de los cinco bloques que determinan el coste unitario real (escandallo o BOM, precios de compra actualizados por proveedor, tiempos reales de MOD por referencia y operario, indirectos repartidos sobre base objetiva y precios de venta vigentes por cliente), devuelve el margen real por referencia y por cliente y calcula el precio mínimo viable para un margen objetivo del 20%. Llegas a cada negociación comercial o a cada subida de tarifa con un número justificado, no con una intuición.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía rápida del caso (este archivo) |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `escandallos.csv` | Materiales y cantidades por referencia (BOM) |
| `precios_compra.csv` | Precios actualizados de materias primas por proveedor |
| `tiempos_produccion.csv` | Minutos de MOD por referencia y operario |
| `indirectos.csv` | Costes indirectos mensuales de la planta |
| `precios_venta.csv` | PVP actual por referencia y cliente principal |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la guía oficial de Anthropic → https://docs.anthropic.com/en/docs/claude-code — comando de instalación: `npm install -g @anthropic-ai/claude-code`.
2. **Descarga esta carpeta completa** a tu equipo (ej. `C:\Caso_37_Coste_Real_Industrial\`) con los 5 CSVs en la raíz.
3. **Abre la terminal** en esa carpeta y escribe `claude` para arrancar Claude Code.
4. **Arrastra `LEEME.md`, `prompt.txt` y los 5 CSVs** al chat para dar contexto completo antes de ejecutar.
5. **Edita `prompt.txt`** cambiando `[EMPRESA]`, `[MES AÑO]` y rutas, pégalo y pulsa Enter. Obtendrás tabla web interactiva + Excel de escandallo + alertas PDF por referencia deficitaria.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Escandallos / BOM | Precios compra | Tiempos producción | Indirectos | Precios venta |
|---|---|---|---|---|---|
| **SAP Business One / S/4** | CS03 (lista materiales) | ME1L (tarifas proveedor) | CA03 (hoja de ruta) | CO-OM (centros coste) | VK13 (tarifas venta) |
| **A3 ERP (Wolters Kluwer)** | Fabricación → Escandallos | Compras → Tarifas proveedor | Fabricación → Rutas | Contabilidad analítica | Ventas → Tarifas |
| **Sage 200** | Producción → Estructuras | Proveedores → Tarifas | Producción → Fases | Analítica → Centros coste | Ventas → Tarifas |
| **Holded** | Productos → Escandallo | Contactos proveedores → Tarifas | Partes de producción | Gastos recurrentes | Ventas → Tarifas |
| **Odoo** | Fabricación → BOM | Compras → Listas de precios | Fabricación → Operaciones | Contabilidad analítica | Ventas → Listas de precios |
| **Navision / Business Central** | Fabricación → Listas de materiales | Compras → Precios proveedor | Rutas de producción | Dimensiones analíticas | Ventas → Precios |
| **Contasol / ContaPlus** | — (combinar con módulo producción) | Facturas de compra | — | Mayor cuentas grupo 62 | Facturación emitida |

> ⚠️ **Nota de sector:** Diseñado para **PYMEs industriales, metalúrgicas y de fabricación en serie**. Para **mecanizado por encargo** sustituye "unidades producidas" por "horas facturables"; para **hostelería** usa el escandallo de plato en vez de este; para **distribución pura sin fabricación** usa [caso-29 (coste real por referencia en gran distribución)](../caso-29-coste-real-gran-distribucion/), que no requiere tiempos de MOD. Para enlazar coste real con rentabilidad por cliente industrial, combina con [caso-28 (rentabilidad clientes asesoría)](../caso-28-rentabilidad-clientes-asesoria/) adaptando la lógica a cuenta cliente industrial, y con [caso-31 (mantenimiento correctivo)](../caso-31-mantenimiento-correctivo-industrial/) para incorporar el impacto de paros en el coste de MOD.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con **20 años en C-Suite**. Ayudo a **PYMEs españolas de 1-50 M€** del sector **industria, mayoristas y construcción** a automatizar operaciones con IA traduciendo cada mejora a impacto directo en P&L, EBITDA y caja.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **2 o 3 automatizaciones a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min de diagnóstico gratuito:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 GitHub [@isaacromadotes](https://github.com/isaacromadotes)

<sub>coste real producto PYME industrial, escandallo BOM actualizado metalurgia, precio mínimo viable fabricación, Claude Code pricing industrial, margen por referencia metalúrgica, imputación indirectos planta, tiempos MOD fabricación en serie, política de precios PYME industrial, análisis rentabilidad SKU fabricante, consultoría automatización industria metalúrgica España</sub>
