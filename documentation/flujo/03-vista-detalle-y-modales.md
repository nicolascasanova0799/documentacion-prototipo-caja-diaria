---
description: "Vista Detalle, tabla única y modales por concepto"
icon: magnifying-glass
---

# Vista Detalle y modales

**Respuesta primero:** la vista Detalle muestra una sola tabla Descripción/Monto; al hacer clic se abre un modal con columnas según el concepto, alineado al feedback del cliente más que a la imagen apilada del Excel.

{% hint style="info" %}
**Cifras ilustrativas:** los montos, choferes y usuarios de esta página son cifras ilustrativas del prototipo (datos simulados, commit 2ce55a3b). No son datos reales ni cifras validadas.
{% endhint %}

{% hint style="info" %}
**Supuesto del prototipo:** tabla única + modal XL (decisión de prototipo tras feedback); levantamiento permite modal o sección inferior (L §4 Navegación).
{% endhint %}

## Filas en Detalle (prototipo)

Rutas, Efectivo, Cheques, Transferencias, Crédito, Cobranza, GetNet, Notas de crédito, Protestos, Reversos, Total Caja. **No** hay fila Diferencias en Detalle. Egresos en rojo con “-”.

## Inconsistencia conocida

| Comportamiento | Resumen | Detalle | Estado |
|----------------|---------|---------|--------|
| Clic en GetNet | Abre modal | No clicable | Supuesto del prototipo ([Q-13](../preguntas-pendientes.md#q-13)) |

## Maqueta del cliente (referencia)

<figure><img src="../../.gitbook/assets/maqueta-cliente-reporte-detalle.png" alt="Maqueta del cliente del Reporte Caja Diaria, vista Detalle"><figcaption><p>Maqueta del cliente (referencia). No es una captura del prototipo.</p></figcaption></figure>

Compara columnas con [Columnas de detalle](../referencia/columnas-de-detalle.md) (P-04, Q-09, Q-08).

{% hint style="info" %}
**Captura pendiente:** falta agregar la captura del prototipo para vista Detalle y modales. Mientras tanto, revisa la maqueta en la ruta Finanzas > Caja Diaria.
{% endhint %}

## Cómo revisarla

{% stepper %}
{% step %}
### Abre Detalle

Abre la vista **Detalle** desde el filtro y revisa la lista de conceptos.
{% endstep %}

{% step %}
### Abre un modal

Haz clic en un concepto para abrir el modal y revisa título “Detalle &lt;Concepto&gt;”.
{% endstep %}

{% step %}
### Columnas

Compara columnas con [Columnas de detalle](../referencia/columnas-de-detalle.md).
{% endstep %}

{% step %}
### Anota deltas

Anota diferencias (GetNet no clicable, Q-13) y enlaza preguntas abiertas.
{% endstep %}
{% endstepper %}

Siguiente: [Liquidación y control interno](04-liquidacion-control-interno.md).
