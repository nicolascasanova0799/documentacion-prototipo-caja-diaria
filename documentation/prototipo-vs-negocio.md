---
description: "Deltas entre levantamiento, maqueta del cliente y prototipo Angular"
icon: code-compare
---

# Prototipo vs negocio

**Respuesta primero:** el prototipo adelanta pantallas y números simulados; esta tabla marca qué diverge del levantamiento para que no se confunda con reglas cerradas.

{% hint style="info" %}
**Versión revisada:** prototipo rama `prototipo-reporte-caja-diaria`, commit 2ce55a3b. Cambios posteriores pueden no estar reflejados.
{% endhint %}

{% hint style="info" %}
**Cifras ilustrativas:** los montos, choferes y usuarios de esta página son cifras ilustrativas del prototipo (datos simulados, commit 2ce55a3b). No son datos reales ni cifras validadas.
{% endhint %}

| Tema | Levantamiento / imagen | Prototipo | Estado |
|------|------------------------|-----------|--------|
| GetNet captura | Pendiente canal (P-01) | Tres vouchers de ejemplo como ingreso | Pendiente de definición / supuesto en el prototipo |
| GetNet monto | L cita 412.980; IMG 412.900 | 412.900 | Por validar ([Q-07](preguntas-pendientes.md#q-07)) |
| Diferencias | Pendiente evento y fórmula (P-02) | $0 fijo, no clicable, ausente en Detalle | Pendiente de definición |
| Anticipos regla técnica | Por validar consulta | Fila Origen Anticipo en detalle Transferencias | Por validar / ilustrativo |
| Cobranza | Por validar flujo cartera (P-03) | Cash-in facturas anteriores suma a Total Caja | Supuesto del prototipo |
| Valor por defecto del control interno | Por validar (P-05) | Checkbox desmarcado por defecto | Por validar |
| Rango fechas | Máx mes o 30 días confirmado | Solo inicio ≤ fin | Supuesto del prototipo (demo) |
| Exportar / Imprimir | Ambos requeridos | Excel/PDF simulados; sin Imprimir | Por validar ([Q-11](preguntas-pendientes.md#q-11)) |
| Total Caja fórmula | IMG/Excel 76.485.516 incluye Total Rutas | ingresos − egresos sin Total Rutas = 19.761.186 neto | Por validar ([Q-06](preguntas-pendientes.md#q-06)) |
| Total Rutas cifra | L/IMG discrepancias menores | 34.420.754 | Por validar ([Q-07](preguntas-pendientes.md#q-07)) |
| Cheques monto | IMG-R 5.303.368 vs IMG-D 5.503.368 | 5.503.368 | Por validar ([Q-07](preguntas-pendientes.md#q-07)) |
| Protestos / Reversos | Separados en resumen L | Separados en resumen y modales | Confirmado |
| Detalle ítems | IMG-D sin Efectivo; protestos combinados | Agrega Efectivo; separa Protestos/Reversos; Total Caja en detalle | Supuesto del prototipo |
| Rutas columnas | L incluye Reversos; IMG-D no | Sin columna Reversos | Por validar ([Q-09](preguntas-pendientes.md#q-09)) |
| Cheques columnas | Origen Cobranza en IMG-D | Sin Origen; solo recorrido | Por validar ([Q-08](preguntas-pendientes.md#q-08)) |
| Crédito columnas | Chofer, Cliente en IMG-D | Descripción genérica | Supuesto del prototipo |
| Cobranza columnas | Usuario en L | Sin Usuario | Por validar ([Q-09](preguntas-pendientes.md#q-09)) |
| NC columnas | Docto, Fecha, Cliente | Folio, Descripción | Supuesto del prototipo |
| Transferencias columnas | Vacías P-04 | Ocho columnas propuestas | Pendiente de definición |
| Crédito como ingreso | Aparece en ingresos IMG-R | Suma a Total Caja | Por validar |
| Vista detalle UX | Modal o sección inferior | Tabla única + modal | Supuesto del prototipo |
| GetNet clicabilidad | No definido | Clic en Resumen, no en Detalle | Supuesto del prototipo ([Q-13](preguntas-pendientes.md#q-13)) |
| Total Rutas vs medios | No cuadra en ejemplos | Ejemplo ilustrativo sin cuadrar | Por validar ([Q-14](preguntas-pendientes.md#q-14)) |
| Transferencia por corroborar | No es Crédito (L) | Todavía no se sabe en qué línea del resumen cae | Pendiente de definición ([Q-12](preguntas-pendientes.md#q-12)) |

{% hint style="warning" %}
**Por validar:** prioriza [Preguntas pendientes](preguntas-pendientes.md) antes de implementar backend.
{% endhint %}
