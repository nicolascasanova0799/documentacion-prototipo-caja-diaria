---
description: Recorrido completo del operador en el prototipo Caja Diaria
icon: diagram-project
---

# Visión general

**Respuesta primero:** filtras por fechas, eliges Resumen o Detalle y, solo en Detalle, abres el modal de un concepto (GetNet no abre modal por ahora). Puedes exportar (simulado). La liquidación de recorrido es donde nace parte del dato vía control interno.

{% hint style="success" %}
**Confirmado:** navegación en dos niveles (Resumen y Detalle) según levantamiento (L §4 Navegación, N-02). El modal se abre solo desde Detalle ([Q-13](../preguntas-pendientes.md#q-13)).
{% endhint %}

## Recorrido en pasos

{% stepper %}
{% step %}
### Filtrar

Elige **Fecha Inicio** y **Fecha Final** y la vista **Resumen** o **Detalle**. En producción el rango debe estar acotado (mes o 30 días); el prototipo solo valida inicio ≤ fin.
{% endstep %}

{% step %}
### Elegir vista

**Resumen** muestra conceptos con columnas Ingresos/Egresos. **Detalle** muestra una tabla única Descripción/Monto por concepto.
{% endstep %}

{% step %}
### Abrir detalle

En la vista **Detalle**, haz clic en un concepto para abrir el modal. Resumen no abre modal. GetNet no abre modal mientras no esté definida su tabla de detalle ([Q-13](../preguntas-pendientes.md#q-13)).
{% endstep %}

{% step %}
### Exportar

Usa **Exportar** (Excel/PDF simulados en el prototipo). Imprimir está pendiente de definir con el cliente ([Q-11](../preguntas-pendientes.md#q-11)).
{% endstep %}
{% endstepper %}

```mermaid
flowchart LR
  F[Filtro fechas] --> R[Resumen]
  F --> D[Detalle]
  D --> C[Clic concepto]
  C --> M[Modal detalle]
  R --> E[Exportar]
  D --> E
```

## Paso a paso con enlaces

| Paso | Qué hace                            | Página                                                              |
| ---- | ----------------------------------- | ------------------------------------------------------------------- |
| 1    | Contexto y alcance del prototipo    | [Alcance del prototipo](../contexto/alcance-prototipo.md)           |
| 2    | Filtros, vistas, exportación        | [Filtros, vistas y exportación](01-filtros-vistas-y-exportacion.md) |
| 3    | Tabla resumen y maqueta cliente     | [Vista Resumen](02-vista-resumen.md)                                |
| 4    | Tabla detalle y modales             | [Vista Detalle y modales](03-vista-detalle-y-modales.md)            |
| 5    | Origen del checkbox control interno | [Liquidación y control interno](04-liquidacion-control-interno.md)  |
| 6    | Cierre de dudas                     | [Preguntas pendientes](../preguntas-pendientes.md)                  |
