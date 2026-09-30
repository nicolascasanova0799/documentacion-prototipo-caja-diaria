---
description: "Columnas de detalle por concepto: levantamiento, maqueta y prototipo"
icon: table-columns
---

# Columnas de detalle

**Respuesta primero:** cada concepto puede tener columnas distintas según la fuente; esta tabla cruza levantamiento, imagen del cliente y configuración del prototipo para detectar huecos (Transferencias, Rutas, Cobranza).

{% hint style="info" %}
**Cifras ilustrativas:** los montos, choferes y usuarios de esta página son cifras ilustrativas del prototipo (datos simulados, commit 2ce55a3b). No son datos reales ni cifras validadas.
{% endhint %}

Las capturas de maqueta están en [Vista Detalle y modales](../flujo/03-vista-detalle-y-modales.md); aquí solo texto.

| Concepto | Levantamiento / IMG-D | Prototipo (finanza.config) | Notas / enlace |
|----------|----------------------|----------------------------|----------------|
| Rutas | Recorrido, chofer, venta, medios de pago; L menciona Reversos | Recorrido, Chofer, Venta, Cheques, Crédito, Transferencia, N/C, Efectivo, Usuario | [Q-09](../preguntas-pendientes.md#q-09) (¿Reversos?) |
| Efectivo | Monto por ruta | Recorrido, Descripción, Monto | Confirmado en espíritu |
| Cheques | N° Docto, Banco, Cliente, Monto (L); IMG-D: Origen Ruta/Cobranza, Usuario | Recorrido, Banco, N° cheque, Monto | [Q-08](../preguntas-pendientes.md#q-08) Origen Cobranza vs solo Ruta |
| Transferencias | Columnas vacías en Excel/IMG-D | Fecha, N° comprobante, Banco origen, RUT, Cliente, Docto, Monto, Origen (Ruta\|Anticipo) | [P-04](../preguntas-pendientes.md#p-04) |
| Crédito | Recorrido, chofer, cliente, monto (IMG-D) | Recorrido, Descripción, Monto | [Q-09](../preguntas-pendientes.md#q-09) |
| Cobranza | Rut cliente, Docto, fechas emisión/vcto, Monto, Usuario (L) | Cliente, Documento, Nota, Monto | [Q-09](../preguntas-pendientes.md#q-09) (¿Usuario?) |
| GetNet | — | Fecha, N° voucher, Cliente, Monto, Usuario | [P-01](../preguntas-pendientes.md#p-01) |
| NC | Docto, Fecha, Cliente, Monto | Folio, Descripción, Monto | [Q-09](../preguntas-pendientes.md#q-09) |
| Protestos | Docto, Fecha, Cliente, Monto | Docto, Fecha, Cliente, Monto | Alineado a IMG-D |
| Reversos | Docto, Fecha, Cliente, Monto | Docto, Fecha, Cliente, Monto | Separado de Protestos en resumen (OK con L) |

{% hint style="danger" %}
**Pendiente de definición:** el negocio todavía no define esta regla para columnas finales de Transferencias ([P-04](../preguntas-pendientes.md#p-04)) y otros conceptos ([Q-09](../preguntas-pendientes.md#q-09)).
{% endhint %}
