# Caso 04 · Entrada Automática de Facturas de Proveedor — De 3 minutos a 30 segundos por factura

> Pack listo para gestorías, asesorías y departamentos de administración. Resultado: factura PDF leída, asiento contable generado y CSV listo para A3/Holded. Ahorro medio: 4h 15min/día (85 facturas × 3 min).

## 🎯 Problema que resuelve

Una gestoría o departamento de administración de 15 personas procesa unas 85 facturas al día. A 3 min por factura (abrir PDF, buscar proveedor, asignar cuentas, teclear líneas, cuadrar), son **4h 15min diarios tecleando** — trabajo cualificado desperdiciado en tarea repetitiva. Este pack lee el PDF, extrae datos, cruza CIF contra el maestro de proveedores, asigna cuentas según plan contable, genera el asiento Debe/Haber y alerta si hay facturas pendientes del proveedor.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía original del caso |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `factura_proveedor.pdf` | Factura ficticia de ejemplo |
| `maestro_proveedores.csv` | Maestro con CIF, cuentas, forma de pago |
| `plan_contable.csv` | PGC español simplificado (gasto, IVA, tesorería) |

## 🚀 Cómo usarlo en 5 pasos

1. **Descarga** los archivos de esta carpeta.
2. **Abre** `prompt.txt` y cópialo.
3. **Pégalo** en Claude Code ([instalación aquí](https://docs.anthropic.com/en/docs/claude-code)).
4. **Cambia** `[EMPRESA]`, `[MES AÑO]` y `@ruta/` por tus datos reales.
5. **Pulsa Enter**: en 30-60 segundos tienes asiento contable + CSV listo para importar.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Maestro proveedores | Plan contable |
|---|---|---|
| **A3 / A3ERP** | Ficheros → Proveedores → Exportar | Contabilidad → Plan de cuentas → Exportar |
| **Sage 50 / 200** | Maestros → Proveedores → Excel | Contabilidad → Plan contable → Listado |
| **Holded** | Contactos → Proveedores → CSV | Contabilidad → Plan de cuentas → CSV |
| **SAP Business One** | Interlocutores → Proveedores → Exportar | Finanzas → Plan de cuentas → Exportar |
| **Odoo** | Compras → Proveedores → Exportar | Contabilidad → Configuración → Plan contable |
| **Contaplus / Sage Despachos** | Plan contable → Grupo 40 → Exportar | PGC → Cuentas → Exportar |

⚠️ **Diseñado para gestorías, asesorías y administración** con PGC español. Si usas plan sectorial o cuentas personalizadas, sustituye `plan_contable.csv` por el tuyo. El asiento usa formato Debe/Haber compatible con A3, Holded y la mayoría de programas contables españoles.

## 📞 ¿Quieres implementarlo en tu empresa?

Soy **Isaac Romà**, economista y ex-CEO/CFO/COO con 20 años en C-Suite. Ayudo a PYMEs españolas (1-50M€) de industria, mayoristas y construcción a automatizar su gestión con IA.

**Servicios:**
- 🔍 **Diagnóstico de automatización**: 750€
- ⚙️ **Automatización llave en mano**: desde 4.500€
- 🤝 **Acompañamiento mensual**: 300€/mes

👉 **Reserva 30 min gratis**: [calendly.com/asesor-online-ia/30min](https://calendly.com/asesor-online-ia/30min)

---

**Isaac Romà** · Consultor de automatización IA para PYMEs
🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://linkedin.com/in/isaacroma) · 💻 [GitHub](https://github.com/isaacromadotes)

---

<sub>**Keywords**: entrada facturas automática, OCR facturas proveedor, asientos contables IA, Claude Code gestoría, automatización asesoría contable, A3 importación facturas, Holded facturas automatizadas, PGC asiento automático, factura PDF a asiento, consultor automatización gestoría España.</sub>
