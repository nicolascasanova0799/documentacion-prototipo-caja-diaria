---
description: "Filtros de fecha, vistas Resumen/Detalle y exportación en el prototipo"
icon: filter
---

# Filtros, vistas y exportación

**Respuesta primero:** el prototipo exige fechas válidas (inicio ≤ fin), acepta el mes completo si ambas fechas son del mismo mes y, si cruzan de mes, como máximo 30 días. Exportar simula Excel e Imprimir simula PDF.

{% hint style="success" %}
**Confirmado:** Fecha Inicio, Fecha Final y vistas Resumen y Detalle (L §4). Exportar e imprimir son requeridos a nivel negocio (L §4, RFP-05).
{% endhint %}

{% hint style="info" %}
**Confirmado:** rango por defecto = inicio del mes actual hasta hoy. Mismo mes calendario permite el mes completo (incluido uno de 31 días). Meses distintos: máximo 30 días ([Q-10](../preguntas-pendientes.md#q-10)). Exportar = Excel e Imprimir = PDF ([Q-11](../preguntas-pendientes.md#q-11)).
{% endhint %}

## Comportamiento en el prototipo (2ce55a3b)

| Elemento | Prototipo | Estado |
|----------|-----------|--------|
| Radio Resumen / Detalle | Resumen por defecto; cambio dispara búsqueda si el formulario es válido | Supuesto del prototipo |
| Botón Buscar | Presente además del auto-disparo | Supuesto del prototipo |
| Datos devueltos | Siempre el mismo fixture sin importar el rango | Supuesto del prototipo |
| Límite de rango | Mismo mes completo; entre meses, máximo 30 días. La búsqueda no corre si se excede | Confirmado ([Q-10](../preguntas-pendientes.md#q-10)) |
| Exportar | Botón Exportar; toast de Excel simulado | Confirmado ([Q-11](../preguntas-pendientes.md#q-11)) |
| Imprimir | Botón Imprimir; toast de PDF simulado | Confirmado ([Q-11](../preguntas-pendientes.md#q-11)) |

{% hint style="success" %}
**Confirmado:** enero completo (1 al 31) es válido. Del 1 de enero al 1 de febrero no: son meses distintos y suman más de 30 días.
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

Prueba un mes completo de 31 días (válido) y un cruce de meses de más de 30 días (la búsqueda no corre).
{% endstep %}

{% step %}
### Prueba exportar

Prueba **Exportar** (Excel simulado) e **Imprimir** (PDF simulado).
{% endstep %}
{% endstepper %}

Continúa en [Vista Resumen](02-vista-resumen.md).
