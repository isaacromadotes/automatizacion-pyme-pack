# Caso 05 · Trazabilidad de Lote en Segundos — Responde a Sanidad en minutos, no en días

> Pack listo para agroalimentario (conservas, cárnicas, lácteos, panadería, bodegas, aceite). Resultado: trazabilidad hacia atrás y hacia adelante del lote + informe PDF para Sanidad en segundos. Cumple Reglamento CE 178/2002.

## 🎯 Problema que resuelve

Recibes alerta sanitaria de AESAN o de un cliente. Tienes **24 horas** para localizar el lote: de qué materias primas venía, cuántas unidades se fabricaron y a qué clientes se enviaron. En la mayoría de PYMEs agroalimentarias esa info está en un cuaderno del jefe de producción, tres Excel que nadie ha cruzado, y un ERP donde nadie sabe hacer el informe. Resultado: horas o días buscando, riesgo de multa (CE 178/2002 art. 18) y pérdida del cliente grande (Mercadona, Consum, Carrefour) por no pasar la próxima auditoría IFS/BRC. Este pack cruza entradas, producción y salidas en segundos.

## 📦 Archivos del pack

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Guía original del caso |
| `prompt.txt` | Prompt listo para pegar en Claude Code |
| `entradas_mp.csv` | Registro de 12 lotes de materia prima de proveedores |
| `produccion.csv` | 8 órdenes de producción de producto terminado |
| `salidas_pt.csv` | 15 albaranes de salida cruzando los lotes a clientes |

## 🚀 Cómo usarlo en 5 pasos

1. **Descarga** los archivos de esta carpeta.
2. **Abre** `prompt.txt` y cópialo.
3. **Pégalo** en Claude Code ([instalación aquí](https://docs.claude.com/claude-code)).
4. **Cambia** el lote a buscar (ejemplo: `L2024-0847`) por el tuyo.
5. **Pulsa Enter**: recibirás web local con buscador + PDF listo para Sanidad.

## 🔌 Cómo exportar los datos desde tu ERP

| ERP | Entradas MP | Producción | Salidas PT |
|---|---|---|---|
| **A3 ERP** | Compras → Albaranes compra | Producción → Órdenes fabricación | Ventas → Albaranes venta |
| **Sage 200** | Compras → Recepción mercancía | Producción → Partes fabricación | Ventas → Albaranes |
| **Holded** | Inventario → Movimientos entrada | (sin módulo producción) | Ventas → Albaranes |
| **SAP Business One** | Compras → GRPO | Producción → Órdenes fabricación | Ventas → Entrega |
| **Odoo** | Inventario → Recepciones | Fabricación → Órdenes | Inventario → Entregas |

💡 Los nombres de columna no tienen que coincidir: Claude Code los interpreta.

⚠️ **Diseñado para agroalimentario** (CE 178/2002 "one step back, one step forward"). Para cosmética, farmacia, químico o pintura, cambia `temperatura_esterilizacion` por tu parámetro crítico (pH, viscosidad, densidad) y `certificado_calidad` por tu registro (COA, CoC). Dile el sector a Claude Code al inicio del prompt y ajusta solo.

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

<sub>**Keywords**: trazabilidad lote agroalimentario, Reglamento CE 178/2002, auditoría IFS BRC, alerta AESAN respuesta, trazabilidad conservera cárnica, Claude Code agroalimentario, informe Sanidad automático, trazabilidad hacia atrás adelante, Mercadona proveedor auditoría, consultor automatización agroalimentaria España.</sub>
