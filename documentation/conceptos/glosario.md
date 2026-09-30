---
description: Términos del Reporte Caja Diaria con estado de definición
icon: book
---

# Glosario

**Respuesta primero:** usa esta tabla para alinear lenguaje con el levantamiento; cada término indica si la regla está confirmada, por validar o pendiente.

## Leyenda de estados

| Estado                  | Significado                                                     |
| ----------------------- | --------------------------------------------------------------- |
| Confirmado              | Acordado en levantamiento y/o maqueta del cliente               |
| Por validar             | Falta confirmación del cliente antes de construir               |
| Pendiente de definición | El negocio aún no define la regla                               |
| Supuesto del prototipo  | Así lo muestra el prototipo para revisión; no es regla acordada |

| Término                  | Definición breve                                                                                                  | Estado                  |
| ------------------------ | ----------------------------------------------------------------------------------------------------------------- | ----------------------- |
| Ruta                     | Recorrido liquidado; origen de efectivo, cheques y parte de transferencias                                        | Confirmado              |
| Liquidación de recorrido | Proceso de cierre donde se registran medios de pago de la ruta                                                    | Confirmado              |
| Pago Directo             | Módulo de ingreso manual; no es línea de medio de pago                                                            | Confirmado              |
| Anticipo                 | Pago vía Pago Directo sobre factura de ruta del mismo día                                                         | Confirmado              |
| Cobranza                 | Cobros de facturas anteriores fuera de la recaudación del recorrido                                               | Por validar             |
| Cobro vendedor           | Sinónimo operativo de **Crédito** en el resumen                                                                   | Confirmado              |
| Control interno          | Checkbox en liquidación con motivos (transferencia por corroborar, cheque por regularizar, pendiente de depósito) | Confirmado              |
| GetNet                   | Ingresos POS / vouchers GetNet en el resumen                                                                      | Pendiente de definición |
| NC                       | Notas de crédito como egreso                                                                                      | Confirmado              |
| Protesto                 | Cheques protestados como egreso                                                                                   | Confirmado              |
| Reverso                  | Reversos de documentos como egreso                                                                                | Confirmado              |
| Diferencias              | Línea de egreso para cuadraturas / faltantes                                                                      | Pendiente de definición |
| Total Rutas              | Venta consolidada de rutas liquidadas del día (informativo)                                                       | Confirmado              |
| Total Caja               | Cierre del reporte; **fórmula por validar**                                                                       | Por validar             |

{% hint style="danger" %}
**Pendiente de definición:** el negocio todavía no define cómo se captura GetNet ni si se registra monto bruto o líquido. Bloquea el desarrollo del backend.
{% endhint %}

Ver detalle en [P-01](../preguntas-pendientes.md#p-01) y fila GetNet en [Líneas del reporte](../referencia/lineas-del-reporte.md).
