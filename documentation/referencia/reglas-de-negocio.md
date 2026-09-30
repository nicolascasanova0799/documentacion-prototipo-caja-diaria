---
description: Reglas confirmadas del levantamiento y supuestos del prototipo
icon: scale-balanced
---

# Reglas de negocio

**Respuesta primero:** la exclusividad de ruta para efectivo/cheques y la naturaleza de Pago Directo están confirmadas; el prototipo añade reglas de cálculo que aún no son negocio cerrado.

{% hint style="info" %}
**Cifras ilustrativas:** los montos, choferes y usuarios de esta página son cifras ilustrativas del prototipo (datos simulados, commit 2ce55a3b). No son datos reales ni cifras validadas.
{% endhint %}

## Confirmadas

| Regla                      | Descripción                                                                          |
| -------------------------- | ------------------------------------------------------------------------------------ |
| Exclusividad de Ruta       | Efectivo y cheques del resumen provienen **solo** de ruta                            |
| Pago Directo               | Módulo de ingreso manual; **no** es medio de pago en el resumen                      |
| Anticipo vs Cobranza       | Misma factura en ruta del día → Anticipo; factura anterior → Cobranza                |
| Crédito vs control interno | Crédito = cobro vendedor sin control interno; transferencia por corroborar ≠ crédito |
| Rango acotado              | Consulta limitada a mismo mes o máximo 30 días                                       |
| Exportar e imprimir        | Debe permitir exportar e imprimir                                                    |
| NC, Protestos, Reversos    | Tratados como egresos validados                                                      |

## Supuesto del prototipo

| Regla en el prototipo                                                        | Notas                                                                    |
| ---------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| Ingresos = Efectivo + Cheques + Transferencias + Crédito + Cobranza + GetNet | Crédito suma a Total Caja — validar si es dinero en caja                 |
| Egresos = NC + Protestos + Reversos                                          | Confirmado como egresos                                                  |
| Diferencias = 0 fijo                                                         | Pendiente negocio (P-02)                                                 |
| Total Caja = ingresos − egresos **sin** incluir Total Rutas                  | Contrasta con Excel 76.485.516 ([Q-06](../preguntas-pendientes.md#q-06)) |
| Cobranza como dinero cobrado hoy por facturas anteriores                     | [P-03](../preguntas-pendientes.md#p-03)                                  |
| Fixture único para cualquier rango de fechas                                 | Demo offline                                                             |

{% hint style="info" %}
**Supuesto del prototipo:** así lo muestra la maqueta para poder revisarla; no es una regla acordada.
{% endhint %}

{% hint style="warning" %}
**Por validar:** fórmula oficial de Total Caja. No marques como Confirmado el neto **19.761.186** ni el **76.485.516** del Excel; el segundo es valor del Excel del cliente, en revisión.
{% endhint %}

<details>

<summary>Bordes</summary>

Reglas de otros reportes financieros quedan fuera de este documento.

</details>
