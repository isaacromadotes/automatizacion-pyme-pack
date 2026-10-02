# Caso 14 · Rentabilidad real por cliente — Detecta al "gran cliente" que te descapitaliza

> En la demo (Suministros Levante S.L., 25 clientes), el **nº 2 en facturación (480.000 €/año)** sale **último en rentabilidad**: pierde **12.000 €/año**.

## 🎯 Problema que resuelve

En una PYME mayorista, industrial o de construcción el ranking de clientes por facturación se mira cada mes, pero el de rentabilidad real casi nadie lo tiene. Y lo peor es que **no coinciden**: un cliente puede ser el nº 2 en ventas y estar generando pérdidas porque exige márgenes del 15%, devuelve más de lo normal, pide entregas urgentes que disparan el coste logístico y paga a 90 días mientras tú financias a proveedor a 30. Multiplicado por 12 meses, ese "gran cliente" es el que te descapitaliza silenciosamente mes a mes. Este pack cruza 4 exports estándar del ERP (ventas, devoluciones, entregas, cobros) y calcula la rentabilidad real cliente a cliente restando coste de producto, devoluciones, coste logístico diferencial y coste financiero del DSO. Genera un cuadro de mandos HTML visual, un Excel con la matriz de 4 cuadrantes (facturación × rentabilidad) y la ficha del cliente menos rentable con simulación de renegociación de precios y plazos de cobro. Convierte una intuición ("creo que este cliente nos cuesta dinero") en un número exacto que puedes llevar a la reunión de renegociación.

## 📦 Archivos del pack

| Archivo | Descripción |
|---|---|
| `LEEME.md` | Documento inicial con la explicación del caso. |
| `prompt.txt` | Prompt listo para pegar en Claude Code. |
| `ventas_cliente.csv` | 25 clientes con facturación, coste de producto y margen bruto. |
| `devoluciones.csv` | Devoluciones anuales por cliente (importe, número, motivo). |
| `entregas.csv` | Nº de entregas totales, urgentes y coste logístico por cliente. |
| `cobros.csv` | Saldo pendiente, DSO, facturas vencidas e importe vencido por cliente. |

## 🚀 Cómo usarlo en 5 pasos

1. **Instala Claude Code** siguiendo la [documentación oficial](https://docs.anthropic.com/en/docs/claude-code): `npm install -g @anthropic-ai/claude-code`
2. **Descomprime este pack** en una carpeta local (ej. `C:\Caso_14_Rentabilidad\`) y abre la terminal dentro de ella con el comando `claude`.
3. **Arrastra a la ventana de Claude Code** el `LEEME.md`, el `prompt.txt` y los 4 CSV (los de demo o los tuyos exportados del ERP con las mismas columnas).
4. **Copia el contenido de `prompt.txt`**, pégalo en Claude Code y sustituye `[EMPRESA]` y `[MES AÑO]` por tus datos reales.
5. **Pulsa Enter**: Claude Code valida los archivos, calcula la rentabilidad real cliente a cliente, levanta el cuadro de mandos HTML en servidor local, genera el Excel con la matriz de 4 cuadrantes y te devuelve la URL y las rutas de los ficheros.

## 🔌 Cómo exportar los datos desde tu ERP

| Dato | A3 / Sage 50 | Holded | SAP Business One | Odoo |
|---|---|---|---|---|
| Facturación y coste por cliente | Ventas → Estadísticas por cliente → Exportar CSV | Ventas → Informes → Ventas por cliente | Ventas → Informe de ventas por cliente | Ventas → Informes → Ventas |
| Devoluciones | Facturas rectificativas / Abonos por cliente | Facturas rectificativas | Devoluciones de clientes | Devoluciones (albaranes de retorno) |
| Entregas y coste logístico | Logística → Albaranes por cliente | Envíos | Ventas → Entregas | Inventario → Transferencias |
| DSO y vencidos | Cartera → Antigüedad de saldos | Cobros → Antigüedad | Financiero → Cartera clientes | Contabilidad → Antigüedad cuentas por cobrar |

> ⚠️ **Nota de sector:** este pack está pensado para **PYMEs mayoristas, distribuidoras, industriales y de construcción B2B** con coste logístico relevante y plazos de cobro significativos. Si tu negocio es retail, e-commerce o servicios puros, la fórmula se ajusta. Para profundizar en palancas concretas, combina este caso con el [caso-06 (análisis básico de rentabilidad por cliente)](../caso-06-rentabilidad-clientes/) y el [caso-08 (control de DSO y cobros)](../caso-08-cobros-dso/).

## 📞 ¿Quieres implementarlo en tu empresa?

**Isaac Romà** — economista, ex-CEO/CFO/COO, 20 años en C-Suite.
Ayudo a **PYMEs industriales, mayoristas y de construcción (1-50M€)** a automatizar operaciones y recuperar margen con IA aplicada al negocio real, no a la tecnología.

- 🔍 **Diagnóstico inicial:** 750 €
- ⚙️ **Automatización a medida:** desde 4.500 €
- 🤝 **Acompañamiento mensual:** 300 €/mes

👉 **Reserva 30 min conmigo:** https://calendly.com/asesor-online-ia/30min

---

🌐 [isaacroma.com](https://isaacroma.com) · 💼 [LinkedIn](https://www.linkedin.com/in/isaacroma) · 💻 [GitHub @isaacromadotes](https://github.com/isaacromadotes)

<sub>rentabilidad real por cliente pyme, análisis rentabilidad clientes b2b, cliente más rentable mayorista, matriz rentabilidad clientes construcción, coste de servir cliente industrial, clientes que generan pérdidas pyme, rentabilidad vs facturación cliente, cuadro de mandos rentabilidad clientes, análisis margen neto cliente pyme, renegociación precios cliente no rentable</sub>
