---
description: "Checkbox Agregar a control interno en liquidación de recorrido"
icon: clipboard-check
---

# Liquidación y control interno

**Respuesta primero:** en liquidación de recorrido puedes marcar “Agregar a control interno” con tres motivos; el crédito (cobro vendedor) no usa ese camino, y el valor por defecto del checkbox sigue por validar.

{% hint style="success" %}
**Confirmado:** motivos Transferencia por corroborar, Cheque por regularizar y Pendiente de depósito (L §3). Crédito = cobro vendedor **sin** control interno; si hay control interno por transferencia, no es crédito sino validación (L §4 Crédito).
{% endhint %}

## Motivos del checkbox

| Motivo | Intención |
|--------|-----------|
| Transferencia por corroborar | Transferencia en validación. Se cuenta en la línea Transferencias, no en Crédito |
| Cheque por regularizar | Cheque pendiente de regularización |
| Pendiente de depósito | Efectivo o cheque aún no depositado |

{% hint style="warning" %}
**Por validar:** valor por defecto del checkbox (legacy premarcado; Manu prefiere desmarcado; prototipo ya desmarcado). Ver [P-05](../preguntas-pendientes.md#p-05).
{% endhint %}

{% hint style="success" %}
**Confirmado:** la transferencia “por corroborar” entra al ítem Transferencias del resumen ([Q-12](../preguntas-pendientes.md#q-12)).
{% endhint %}

{% hint style="info" %}
**Captura pendiente:** falta agregar la captura del prototipo para liquidación y control interno. Mientras tanto, revisa la maqueta en la ruta Finanzas > Caja Diaria.
{% endhint %}

## Cómo revisarla

{% stepper %}
{% step %}
### Abre liquidación

Abre una liquidación de recorrido de ejemplo desde el menú del prototipo.
{% endstep %}

{% step %}
### Marca control interno

Marca **Agregar a control interno** y elige un motivo de la lista.
{% endstep %}

{% step %}
### Crédito sin control interno

Confirma que **Crédito** no pasa por control interno en el flujo acordado.
{% endstep %}

{% step %}
### Opina sobre el valor por defecto

Opina sobre el valor por defecto del checkbox (P-05) y vuelve a [Visión general](vision-general.md) para cerrar el recorrido.
{% endstep %}
{% endstepper %}
