# TurnoSalud — Acta de cierre académico

| Control documental | Detalle                                |
| ------------------ | -------------------------------------- |
| Código             | TS-CIE-01                              |
| Versión y fecha    | v1.0.0 · 23/11/2026                    |
| Responsable        | Sandoval Fernando, gestor del proyecto |
| Revisor interno    | Toapanta, responsable de pruebas       |
| Estado             | En elaboración                         |
| Aprobación interna | Pendiente de revisión en GitHub        |

## 1. Objeto

Revisar los resultados de los puntos 4, 5 y 6 y establecer cuándo puede darse por cerrada la entrega académica. Las decisiones del cliente, la ejecución técnica y las horas de trabajo corresponden al escenario simulado. La evidencia real de revisión interna será el historial de Pull Requests del equipo.

## 2. Balance de la entrega

| Punto         | Evidencia                                                       | Resultado                                                                                                                                             |
| ------------- | --------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| 4. Validación | [Acta de requisitos](../04-validacion/validacion-requisitos.md) | RF-01, RF-02 y RF-03 quedaron definidos con criterios verificables. Recepción aclaró qué debe ocurrir al competir por un horario o cancelar un turno. |
| 5. Cambio     | [Solicitud SC-01](../05-cambio/solicitud-cambio.md)             | Se incorporó al escenario la reprogramación RF-04. Se estimaron ocho horas-persona y se fijaron tres pruebas de aceptación.                           |
| 6. Retrabajo  | [Medición y defecto D-01](medicion-retrabajo.md)                | Se registraron cuatro horas-persona de retrabajo dentro de un bloque de 40. Resultado: 10 %. D-01 figura cerrado en la simulación.                    |

## 3. Plazo, presupuesto y lección aprendida

El plan de referencia contempla 12 semanas y USD 18.000. SC-01 se consideró viable bajo el supuesto de ocho horas disponibles. Las cuatro horas posteriores de retrabajo explican una desviación respecto del esfuerzo inicialmente previsto para el cambio. El caso carece de un registro global de horas, costos y fechas reales que permita afirmar el cumplimiento final de plazo o presupuesto.

El defecto mostró que verificar una reprogramación exige comprobar dos extremos: que el nuevo horario quede correctamente asignado y que el original se conserve cuando el traslado falle. En el siguiente ciclo se definirán ambas comprobaciones durante la revisión del requisito.

## 4. Decisión de cierre

Se propone el cierre de la entrega académica. La conformidad simulada de recepción corresponde al contenido funcional. La aprobación documental queda a cargo de los revisores internos designados.

| Condición para cerrar                                        | Responsable de comprobarla | Situación al emitir v1.0.0               |
| ------------------------------------------------------------ | -------------------------- | ---------------------------------------- |
| Validación, cambio y medición aprobados e integrados en main | Sandoval Fernando          | Pendiente de comprobar en el repositorio |
| Cálculo del 10 % y estado de D-01 coherentes con la medición | Toapanta                   | Pendiente de revisión del acta           |
| Acta aprobada e integrada y enlaces funcionales              | Sandoval Fernando          | Pendiente                                |

Se registrara el cierre efectivo cuando pueda identificar los PR integrados y la fecha del cierre. La presente versión queda preparada para su revisión.

## 5. Historial

| Versión | Fecha      | Responsable       | Descripción                                                      | Estado         |
| ------- | ---------- | ----------------- | ---------------------------------------------------------------- | -------------- |
| v1.0.0  | 23/11/2026 | Sandoval Fernando | Consolidación de resultados y propuesta de cierre de la entrega. | En elaboración |
