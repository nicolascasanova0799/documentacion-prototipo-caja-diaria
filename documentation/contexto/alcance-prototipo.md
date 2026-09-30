---
description: Qué incluye y qué no incluye el prototipo offline de Caja Diaria
icon: bullseye
---

# Alcance del prototipo

**Respuesta primero:** el prototipo es solo lectura, con datos simulados fijos, exportación simulada y menú en Finanzas > Caja Diaria; sirve para revisión antes del backend.

{% hint style="info" %}
**Versión revisada:** prototipo rama `prototipo-reporte-caja-diaria`, commit 2ce55a3b. Cambios posteriores pueden no estar reflejados.
{% endhint %}

{% hint style="success" %}
**Confirmado:** acordado en el levantamiento y en la maqueta del cliente.
{% endhint %}

## Dentro del prototipo

| Aspecto      | Comportamiento                                                                                             | Estado                                                   |
| ------------ | ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| Datos        | Datos simulados fijos; cualquier rango de fechas válido devuelve los mismos montos (fecha fija 15-03-2026) | Supuesto del prototipo                                   |
| Conectividad | Sin GraphQL ni ERP real; Angular 20 offline                                                                | Supuesto del prototipo                                   |
| Lectura      | Solo consulta; no persiste cambios de negocio                                                              | Confirmado (plan L §9)                                   |
| Vistas       | Resumen y Detalle con modales por concepto                                                                 | Supuesto del prototipo                                   |
| Exportación  | Botones Excel y PDF muestran toast de exportación simulada                                                 | Supuesto del prototipo                                   |
| Impresión    | No hay botón Imprimir                                                                                      | Delta vs L (ver [Q-11](../preguntas-pendientes.md#q-11)) |
| Ruta de menú | Finanzas > Caja Diaria                                                                                     | Prototipo (2ce55a3b)                                     |

## Fuera del prototipo (esta documentación)

* Backend, SQL y APIs de producción.
* Capturas de pantalla del prototipo (ver avisos “Captura pendiente” en flujo).

## Plan acordado

1. **Prototipo primero** con datos simulados para alinear pantallas y preguntas.
