---
description: Cada línea del resumen con origen, regla y estado
icon: list-ol
---

# Líneas del reporte

**Respuesta primero:** doce filas en el resumen; efectivo y cheques son solo ruta, las transferencias incluyen anticipos y la transferencia por corroborar, GetNet y Diferencias siguen pendientes, y Total Caja no tiene fórmula confirmada.

{% hint style="info" %}
**Cifras ilustrativas:** los montos, choferes y usuarios de esta página son cifras ilustrativas del prototipo (datos simulados, commit 2ce55a3b). No son datos reales ni cifras validadas.
{% endhint %}

| Línea            | Origen / regla                                                                              | Estado                  |
| ---------------- | ------------------------------------------------------------------------------------------- | ----------------------- |
| Efectivo         | Solo liquidación de ruta; excluye Pago Directo                                              | Confirmado              |
| Cheques          | Solo ruta                                                                                   | Confirmado              |
| Transferencias   | Ruta + anticipos + cobro vendedor con “transferencia por corroborar”                        | Confirmado              |
| GetNet           | Transferencias por GetNet de Santander; captura y bruto/líquido sin definir                 | Pendiente de definición |
| Crédito          | Cobro vendedor en ruta, sin control interno                                                 | Confirmado              |
| Notas de crédito | Egreso                                                                                      | Confirmado              |
| Protestos        | Egreso                                                                                      | Confirmado              |
| Reversos         | Egreso                                                                                      | Confirmado              |
| Diferencias      | Egreso; evento y fórmula desconocidos                                                       | Pendiente de definición |
| Total Rutas      | Venta consolidada rutas liquidadas; informativo                                             | Confirmado              |
| Cobranza         | Facturas anteriores fuera de recaudación de recorridos                                      | Por validar             |
| Total Caja       | Existe la línea; **fórmula por validar**                                                    | Por validar             |

{% hint style="danger" %}
**Pendiente de definición:** el negocio todavía no define cómo se captura GetNet ni si se registra monto bruto o líquido. Bloquea el desarrollo del backend.
{% endhint %}

{% hint style="warning" %}
**Por validar:** fórmula de Total Caja ([Q-06](../preguntas-pendientes.md#q-06)). El Excel del cliente muestra **76.485.516** como valor del Excel del cliente, en revisión (posible inclusión de Total Rutas). El prototipo usa ingresos − egresos sin Total Rutas → **Supuesto del prototipo**.
{% endhint %}

{% hint style="warning" %}
**Por validar:** montos de Cobranza y su relación con Pago Directo ([P-03](../preguntas-pendientes.md#p-03)).
{% endhint %}
