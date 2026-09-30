---
description: 'De dónde sale cada ingreso: ruta, Pago Directo, anticipo y cobranza'
icon: money-bill-transfer
---

# Origen del dinero

**Respuesta primero:** el efectivo y los cheques del resumen son solo de ruta; Pago Directo es un módulo de ingreso manual y clasifica el pago en Anticipo o Cobranza según la factura.

{% hint style="info" %}
**Cifras ilustrativas:** los montos, choferes y usuarios de esta página son cifras ilustrativas del prototipo (datos simulados, commit 2ce55a3b). No son datos reales ni cifras validadas.
{% endhint %}

## Tabla de decisiones

| Origen                          | Qué es                                                                         | Regla principal                                                                                                               | Estado                                          |
| ------------------------------- | ------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| Ruta / liquidación de recorrido | Pagos registrados al cerrar o en el flujo de la ruta del día                   | Efectivo y cheques **solo ruta**; transferencias en ruta **incluyen anticipos** registrados vía Pago Directo antes del cierre | Confirmado                                      |
| Pago Directo                    | Módulo de **ingreso manual** (efectivo, cheque o transferencia)                | **No es un medio de pago** del resumen; es la puerta de entrada al clasificar el dinero                                       | Confirmado                                      |
| Anticipo                        | Transferencia (u otro medio) sobre factura de **ruta del mismo día**           | Se refleja en la línea Transferencias del resumen (concepto anticipo en detalle)                                              | Confirmado (regla de negocio); reflejo numérico |
| Cobranza                        | Cobro de facturas **anteriores** fuera de la recaudación del recorrido del día | Línea de cierre en resumen; detalle y fórmula aún en discusión                                                                | Por validar                                     |
| Cobro vendedor (Crédito)        | Crédito en ruta                                                                | Ingreso en resumen solo **sin** checkbox de control interno                                                                   | Confirmado                                      |
| Transferencia por corroborar    | Cobro vendedor con control interno por ese motivo                              | Se suma en la línea **Transferencias**, no en Crédito                                                                         | Confirmado                                      |

{% hint style="warning" %}
**Por validar:** la regla técnica exacta para identificar anticipos en consultas (fecha factura, estado recorrido, módulo origen) y cómo se ve Anticipo vs Cobranza en totales del resumen.
{% endhint %}

{% hint style="info" %}
**Supuesto del prototipo:** Cobranza se modela como efectivo cobrado hoy por facturas de días anteriores y suma a ingresos de Total Caja; eso no está cerrado con el cliente (ver [P-03](../preguntas-pendientes.md#p-03)).
{% endhint %}
