---
description: "Preguntas abiertas y cerradas del Reporte Caja Diaria (P-01 a P-05, Q-06 a Q-14)"
icon: circle-question
---

# Preguntas pendientes

**Respuesta primero:** la mayoría de las preguntas sigue abierta. Ya quedaron cerradas Q-12 (la transferencia por corroborar entra en la línea Transferencias), P-05 (el checkbox “Agregar a control interno” viene desmarcado por defecto) y Q-13 (el modal solo se abre desde Detalle; GetNet no lo abre mientras no exista su tabla de detalle).

{% hint style="info" %}
**Cifras ilustrativas:** los montos, choferes y usuarios de esta página son cifras ilustrativas del prototipo (datos simulados, commit 2ce55a3b). No son datos reales ni cifras validadas.
{% endhint %}

## Leyenda

| Estado | Uso en esta página |
|--------|-------------------|
| Confirmado | Regla acordada con el cliente |
| Pendiente de definición | Regla de negocio no definida |
| Por validar | Hay evidencia pero falta confirmación del cliente |
| Supuesto del prototipo | Comportamiento del prototipo para revisión |

---

### P-01

**Pregunta:** GetNet — ¿fuente de captura y monto bruto vs líquido?

| | Contenido |
|---|-----------|
| Conocido | La línea existe como ingreso; el prototipo muestra 3 vouchers de ejemplo (412.900 total ilustrativo) |
| Desconocido | Canal (cartola Santander, planilla GetNet, declaración chofer); tratamiento de comisiones |
| Estado | Pendiente de definición |
| Fuente | L §4, L §13, Supuesto 1 |
| Ver también | [Glosario](conceptos/glosario.md), [Líneas del reporte](referencia/lineas-del-reporte.md) |

{% hint style="danger" %}
**Pendiente de definición:** el negocio todavía no define cómo se captura GetNet ni si se registra monto bruto o líquido. Bloquea el desarrollo del backend.
{% endhint %}

---

### P-02

**Pregunta:** Diferencias — ¿evento, fórmula y signo faltante/sobrante?

| | Contenido |
|---|-----------|
| Conocido | La línea existe; en el ejemplo aparece $0 |
| Desconocido | Qué evento la genera, fórmula y si es faltante o sobrante |
| Estado | Pendiente de definición |
| Fuente | L §4, Supuesto 3 |
| Ver también | [Líneas del reporte](referencia/lineas-del-reporte.md) |

{% hint style="danger" %}
**Pendiente de definición:** el negocio todavía no define esta regla.
{% endhint %}

---

### P-03

**Pregunta:** Cobranza — ¿cobrado en el día por facturas anteriores vs saldo de cartera? ¿Pago en oficina va a Cobranza o a Efectivo/Cheques?

| | Contenido |
|---|-----------|
| Conocido | IMG-R: solo facturas anteriores, fuera de recaudación de recorridos; texto sobre cartera impaga y crédito autorizado |
| Desconocido | Cash-in del día vs saldo acumulado; clasificación de pagos en oficina |
| Estado | Por validar |
| Fuente | L §4, Supuesto 2, RR-02, IMG-R |
| Ver también | [Origen del dinero](conceptos/origen-del-dinero.md), [Líneas del reporte](referencia/lineas-del-reporte.md) |

{% hint style="warning" %}
**Por validar:** falta confirmación del cliente antes de construir.
{% endhint %}

---

### P-04

**Pregunta:** ¿Columnas definitivas del detalle de Transferencias?

| | Contenido |
|---|-----------|
| Conocido | Excel e IMG-D vacíos; prototipo propone 8 columnas con Origen Ruta/Anticipo |
| Desconocido | Set final de columnas |
| Estado | Pendiente de definición |
| Fuente | L §4, P |
| Ver también | [Columnas de detalle](referencia/columnas-de-detalle.md) |

{% hint style="danger" %}
**Pendiente de definición:** el negocio todavía no define esta regla.
{% endhint %}

---

### P-05

**Pregunta:** ¿Valor por defecto del checkbox “Agregar a control interno”?

| | Contenido |
|---|-----------|
| Conocido | El checkbox **Agregar a control interno** viene **desmarcado** (desactivado) al abrir el modal. El control interno es una excepción: se marca solo cuando corresponde. El prototipo ya lo muestra así (commit 7a717aa7). |
| Desconocido | — |
| Estado | Confirmado |
| Fuente | L §4 Crédito; aclaración del 30-09-2026 |
| Ver también | [Liquidación y control interno](flujo/04-liquidacion-control-interno.md) |

{% hint style="success" %}
**Confirmado:** “Agregar a control interno” queda desmarcado por defecto. El usuario lo activa solo cuando hay una excepción por corroborar.
{% endhint %}

---

### Q-06

**Pregunta:** ¿Fórmula real de Total Caja (¿incluye Total Rutas? ¿Crédito como dinero en caja)?

| | Contenido |
|---|-----------|
| Conocido | Excel del cliente: **76.485.516** como valor del Excel del cliente, en revisión (parece incluir Total Rutas); prototipo: ingresos − egresos sin Total Rutas |
| Desconocido | Fórmula oficial acordada |
| Estado | Por validar |
| Fuente | IMG-R, XLS, P |
| Ver también | [Vista Resumen](flujo/02-vista-resumen.md), [Reglas de negocio](referencia/reglas-de-negocio.md) |

{% hint style="warning" %}
**Por validar:** falta confirmación del cliente antes de construir.
{% endhint %}

---

### Q-07

**Pregunta:** Discrepancias numéricas entre fuentes (Cheques, Total Rutas, GetNet).

| | Contenido |
|---|-----------|
| Conocido | Cheques 5.303.368 (IMG-R) vs 5.503.368 (IMG-D/prototipo); Total Rutas 34.420.754 vs 34.420.794; GetNet 412.980 (L) vs 412.900 |
| Desconocido | Cuál valor es el correcto por concepto |
| Estado | Por validar |
| Fuente | L §4, IMG-R, IMG-D, P |
| Ver también | [Prototipo vs negocio](prototipo-vs-negocio.md) |

{% hint style="warning" %}
**Por validar:** falta confirmación del cliente antes de construir.
{% endhint %}

---

### Q-08

**Pregunta:** Cheques con Origen “Cobranza” en detalle vs regla “solo Ruta”.

| | Contenido |
|---|-----------|
| Conocido | IMG-D muestra Origen Cobranza en detalle de cheques |
| Desconocido | Si cheques de Pago Directo deben verse en detalle de Cobranza |
| Estado | Por validar |
| Fuente | IMG-D, L §6 |
| Ver también | [Columnas de detalle](referencia/columnas-de-detalle.md) |

{% hint style="warning" %}
**Por validar:** falta confirmación del cliente antes de construir.
{% endhint %}

---

### Q-09

**Pregunta:** Columnas definitivas de Rutas (¿Reversos?), Crédito, Cobranza (¿Usuario?), NC.

| | Contenido |
|---|-----------|
| Conocido | Tres fuentes distintas (L, IMG-D, finanza.config del prototipo) |
| Desconocido | Sets finales por concepto |
| Estado | Pendiente de definición |
| Fuente | L §4, IMG-D, P |
| Ver también | [Columnas de detalle](referencia/columnas-de-detalle.md) |

{% hint style="danger" %}
**Pendiente de definición:** el negocio todavía no define esta regla.
{% endhint %}

---

### Q-10

**Pregunta:** ¿Límite de rango: 30 días corridos o mismo mes calendario?

| | Contenido |
|---|-----------|
| Conocido | Debe existir límite (L, RID-01); prototipo no lo aplica |
| Desconocido | Forma exacta del límite |
| Estado | Por validar |
| Fuente | L §4, RID-01, L §9 |
| Ver también | [Filtros, vistas y exportación](flujo/01-filtros-vistas-y-exportacion.md) |

{% hint style="warning" %}
**Por validar:** falta confirmación del cliente antes de construir.
{% endhint %}

---

### Q-11

**Pregunta:** ¿Imprimir además de exportar? ¿Excel y/o PDF para Resumen y Detalle?

| | Contenido |
|---|-----------|
| Conocido | Levantamiento exige exportar e imprimir; prototipo simula Excel/PDF sin Imprimir |
| Desconocido | Formatos por vista y canal de impresión |
| Estado | Por validar |
| Fuente | L §4, RFP-05 |
| Ver también | [Filtros, vistas y exportación](flujo/01-filtros-vistas-y-exportacion.md) |

{% hint style="warning" %}
**Por validar:** falta confirmación del cliente antes de construir.
{% endhint %}

---

### Q-12

**Pregunta:** Transferencia “por corroborar” — ¿en qué línea del resumen aparece?

| | Contenido |
|---|-----------|
| Conocido | No es Crédito. El levantamiento la trata como transferencia pendiente de validación bancaria y se suma en la línea **Transferencias**. “Transferencias pendientes” no es una fila aparte del resumen. |
| Desconocido | Cómo se marca en el detalle que todavía está por corroborar (eso sigue en [P-04](#p-04)) |
| Estado | Confirmado |
| Fuente | L §4, tabla Motivo de control interno; aclaración del 30-09-2026 |
| Ver también | [Liquidación y control interno](flujo/04-liquidacion-control-interno.md), [Líneas del reporte](referencia/lineas-del-reporte.md) |

{% hint style="success" %}
**Confirmado:** el cobro vendedor con control interno “Transferencia por corroborar” entra al ítem Transferencias del resumen, no a Crédito.
{% endhint %}

---

### Q-13

**Pregunta:** GetNet clicable en Resumen pero no en Detalle — ¿comportamiento deseado?

| | Contenido |
|---|-----------|
| Conocido | El modal de un concepto se abre **solo desde la vista Detalle**, no desde Resumen. GetNet, por ahora, **no abre modal**: aún no está definida la tabla de detalle que se mostraría. |
| Desconocido | Columnas y contenido de esa tabla de GetNet (sigue en [P-01](#p-01)) |
| Estado | Confirmado |
| Fuente | Aclaración del 30-09-2026 |
| Ver también | [Vista Detalle y modales](flujo/03-vista-detalle-y-modales.md), [Vista Resumen](flujo/02-vista-resumen.md) |

{% hint style="success" %}
**Confirmado:** el modal solo se abre desde Detalle. GetNet no abre modal hasta que se defina su tabla de detalle.
{% endhint %}

---

### Q-14

**Pregunta:** Relación Total Rutas (venta) vs suma de medios de pago por ruta.

| | Contenido |
|---|-----------|
| Conocido | En los datos simulados y en la maqueta de detalle los totales no cuadran con la suma de medios |
| Desconocido | Relación esperada en producción |
| Estado | Por validar |
| Fuente | L §4, IMG-D, P |
| Ver también | [Líneas del reporte](referencia/lineas-del-reporte.md) |

{% hint style="warning" %}
**Por validar:** falta confirmación del cliente antes de construir.
{% endhint %}
