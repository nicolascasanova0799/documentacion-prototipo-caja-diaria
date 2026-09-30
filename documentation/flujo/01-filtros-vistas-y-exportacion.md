---
description: "Filtros de fecha, vistas Resumen/Detalle y exportación en el prototipo"
icon: filter
---

# Filtros, vistas y exportación

**Respuesta primero:** el prototipo exige fechas válidas (inicio ≤ fin), alterna Resumen/Detalle al vuelo y simula Excel/PDF; aún no aplica el límite de mes/30 días ni Imprimir.

{% hint style="success" %}
**Confirmado:** Fecha Inicio, Fecha Final y vistas Resumen y Detalle (L §4). Exportar e imprimir son requeridos a nivel negocio (L §4, RFP-05).
{% endhint %}

{% hint style="info" %}
**Supuesto del prototipo:** rango por defecto = inicio del mes actual hasta hoy; solo valida inicio ≤ fin; no bloquea rangos largos.
{% endhint %}

## Comportamiento en el prototipo (2ce55a3b)

| Elemento | Prototipo | Estado |
|----------|-----------|--------|
| Radio Resumen / Detalle | Resumen por defecto; cambio dispara búsqueda si el formulario es válido | Supuesto del prototipo |
| Botón Buscar | Presente además del auto-disparo | Supuesto del prototipo |
| Datos devueltos | Siempre el mismo fixture sin importar el rango | Supuesto del prototipo |
| Excel / PDF | Toast “exportación simulada” | Supuesto del prototipo |
| Imprimir | No existe botón | Delta vs negocio ([Q-11](../preguntas-pendientes.md#q-11)) |

{% hint style="warning" %}
**Por validar:** si el límite es 30 días corridos o el mismo mes calendario ([Q-10](../preguntas-pendientes.md#q-10)).
{% endhint %}

{% hint style="info" %}
**Captura pendiente:** falta agregar la captura del prototipo para filtros y exportación. Mientras tanto, revisa la maqueta en la ruta Finanzas > Caja Diaria.
{% endhint %}

## Cómo revisarla

{% stepper %}
{% step %}
### Elige fechas

Elige **Fecha Inicio** y **Fecha Final** y confirma que el validador rechaza fin anterior a inicio.
{% endstep %}

{% step %}
### Elige vista

Elige la vista **Resumen** o **Detalle** y verifica que cambia la tabla principal.
{% endstep %}

{% step %}
### Revisa el límite de rango

Revisa que el rango respete el límite acordado (Q-10); anota que el prototipo aún no lo enforcea.
{% endstep %}

{% step %}
### Prueba exportar

Prueba **Exportar** (simulado) y confirma qué falta respecto de **Imprimir** (Q-11).
{% endstep %}
{% endstepper %}

Continúa en [Vista Resumen](02-vista-resumen.md).
