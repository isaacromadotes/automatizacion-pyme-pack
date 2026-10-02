# CASO 14 · ¿Tu mejor cliente en facturación te está costando dinero?

## El problema real

En una PYME mayorista, industrial o de construcción, el ranking de clientes por facturación se ve todos los meses. El de rentabilidad **real** por cliente, casi nadie lo tiene.

Y el problema es que **no coinciden**. Un cliente puede ser el número 2 en ventas y estar generando pérdidas por:

- Margen bruto exigido a la baja ("me lo dejas al 15% o me lo compra otro")
- Devoluciones altas ("este pedido no era lo que pedí")
- Entregas urgentes que disparan el coste logístico ("mañana lo necesito en obra")
- DSO (plazo de cobro) que se va a 90 días mientras tú pagas a proveedor a 30

Multiplica eso por 12 meses y el "gran cliente" se convierte en el que **te descapitaliza**.

Este pack cruza los 4 archivos que casi cualquier ERP puede exportar y genera:

1. Un cuadro de mandos HTML espectacular (lo abres en el navegador).
2. Un Excel con la matriz de rentabilidad de 4 cuadrantes.
3. La ficha del cliente menos rentable con simulación de renegociación.

En la demo ficticia (Suministros Levante S.L., 25 clientes), el segundo en facturación (480.000 €/año) sale **último en rentabilidad**: pierde 12.000 €/año.

---

## Qué contiene este ZIP

| Archivo | Qué es |
|---|---|
| `LEEME.md` | Este documento. Léelo primero. |
| `prompt.txt` | El prompt que pegarás en Claude Code. |
| `ventas_cliente.csv` | 25 clientes con facturación, coste de producto y margen bruto. |
| `devoluciones.csv` | Devoluciones anuales por cliente (importe, número, motivo). |
| `entregas.csv` | Nº de entregas totales, urgentes y coste logístico por cliente. |
| `cobros.csv` | Saldo pendiente, DSO, facturas vencidas e importe vencido por cliente. |

---

## Cómo usarlo — paso a paso

**1. Instala Claude Code** (si no lo tienes)
Sigue la guía oficial: https://docs.claude.com/en/docs/claude-code/quickstart

**2. Descomprime este ZIP** en una carpeta de tu ordenador. Por ejemplo:
`C:\Users\tunombre\Downloads\Caso_14_Rentabilidad\`

**3. Abre la terminal en esa carpeta** y escribe:
```
claude
```

**4. Arrastra a la ventana de Claude Code:**
- `LEEME.md`
- `prompt.txt`
- los 4 CSV (o los tuyos con las mismas columnas)

**5. Copia el contenido de `prompt.txt`** y pégalo en Claude Code.

**6. Cambia la variable `[EMPRESA]`** por el nombre de tu empresa (opcional; con los CSV de demo puedes dejarlo como está).

**7. Pulsa Enter** y espera. Claude Code:
- valida los 4 archivos,
- calcula la rentabilidad real cliente a cliente,
- monta el cuadro de mandos HTML y arranca el servidor local,
- genera el Excel con la matriz de 4 cuadrantes,
- te da la URL del cuadro de mandos y las rutas de los ficheros.

---

## De dónde sacar los datos en tu ERP

Los 4 archivos son exports estándar. En la mayoría de ERP se generan en 5 minutos:

| Dato | A3 / Sage 50 | Holded | SAP Business One | Odoo |
|---|---|---|---|---|
| Facturación y coste por cliente | Módulo Ventas → Estadísticas por cliente → Exportar CSV | Ventas → Informes → Ventas por cliente | Módulo Ventas → Informe de ventas por cliente | Ventas → Informes → Ventas |
| Devoluciones | Facturas rectificativas / Abonos por cliente | Facturas rectificativas | Devoluciones de clientes | Devoluciones (albaranes de retorno) |
| Entregas y coste logístico | Módulo Logística → Albaranes por cliente | Envíos | Módulo Ventas → Entregas | Inventario → Transferencias |
| DSO y vencidos | Cartera → Antigüedad de saldos | Cobros → Antigüedad | Módulo Financiero → Cartera clientes | Contabilidad → Antigüedad cuentas por cobrar |

Si no tienes el dato de coste logístico por cliente exacto, aproxima con nº de entregas × coste medio de entrega (te lo dará tu operador logístico o tu gestor de flota).

---

## Nota importante sobre el sector

Este prompt está diseñado para **PYMEs mayoristas, distribuidoras, industriales y de construcción** donde:

- Los clientes son B2B (empresas, no consumidor final).
- Hay coste logístico significativo (entregas físicas).
- El plazo de cobro es una palanca real (facturas a 30/60/90 días).

Si tu negocio es retail puro, e-commerce o servicios, la fórmula de rentabilidad hay que ajustarla. Dímelo y te la adapto en la reunión.

---

## Sobre las variables del prompt

- `[EMPRESA]` → nombre de tu empresa (ej. "Suministros Levante S.L.").
- `[MES AÑO]` → periodo del análisis (ej. "Enero-Diciembre 2025").
- `@ruta/` → si tus CSV están en otra carpeta, cambia las rutas.

---

**Creado por Isaac Romà · https://isaacroma.com**
