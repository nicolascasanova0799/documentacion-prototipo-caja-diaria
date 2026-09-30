---
description: "Términos del Reporte Caja Diaria con estado de definición"
icon: book
---

# Glosario

**Respuesta primero:** usa esta tabla para alinear lenguaje con el levantamiento; cada término indica si la regla está confirmada, por validar o pendiente.

## Leyenda de estados

| Estado | Significado |
|--------|-------------|
| Confirmado | Acordado en levantamiento y/o maqueta del cliente |
| Por validar | Falta confirmación del cliente antes de construir |
| Pendiente de definición | El negocio aún no define la regla |
| Supuesto del prototipo | Así lo muestra el prototipo para revisión; no es regla acordada |

| Término | Definición breve | Estado | Fuente |
|---------|------------------|--------|--------|
| Ruta | Recorrido liquidado; origen de efectivo, cheques y parte de transferencias | Confirmado | L §4 |
| Liquidación de recorrido | Proceso de cierre donde se registran medios de pago de la ruta | Confirmado | L §3, L §4 |
| Pago Directo | Módulo de ingreso manual; no es línea de medio de pago | Confirmado | L §4 |
| Anticipo | Pago vía Pago Directo sobre factura de ruta del mismo día | Confirmado | L §4 |
| Cobranza | Cobros de facturas anteriores fuera de la recaudación del recorrido | Por validar | L §4, P-03 |
| Cobro vendedor | Sinónimo operativo de **Crédito** en el resumen | Confirmado | L §4 |
| Control interno | Checkbox en liquidación con motivos (transferencia por corroborar, cheque por regularizar, pendiente de depósito) | Confirmado | L §3 |
| GetNet | Ingresos POS / vouchers GetNet en el resumen | Pendiente de definición | L §4, P-01 |
| NC | Notas de crédito como egreso | Confirmado | L §4, IMG-R |
| Protesto | Cheques protestados como egreso | Confirmado | L §4 |
| Reverso | Reversos de documentos como egreso | Confirmado | L §4 |
| Diferencias | Línea de egreso para cuadraturas / faltantes | Pendiente de definición | L §4, P-02 |
| Total Rutas | Venta consolidada de rutas liquidadas del día (informativo) | Confirmado | L §4, IMG-R |
| Total Caja | Cierre del reporte; **fórmula por validar** | Por validar | L §4, Q-06 |

{% hint style="danger" %}
**Pendiente de definición:** el negocio todavía no define cómo se captura GetNet ni si se registra monto bruto o líquido. Bloquea el desarrollo del backend.
{% endhint %}

Ver detalle en [P-01](../preguntas-pendientes.md#p-01) y fila GetNet en [Líneas del reporte](../referencia/lineas-del-reporte.md).
