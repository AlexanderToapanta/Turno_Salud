# TurnoSalud — Solicitud de cambio SC-01

| Control documental | Detalle |
|---|---|
| Versión y fecha | v1.0.0 · 23/11/2026 |
| Responsable | Grijalva, líder técnico y programador 1 |
| Revisor interno | Sandoval, gestor del proyecto |
| Estado | En elaboración |
| Aprobación interna | Pendiente de revisión en GitHub |
| Referencia | [Requisitos validados RF-01 a RF-03](../04-validacion/validacion-requisitos.md) |

## 1. Solicitud de recepción

En el escenario simulado, recepción pide trasladar un turno activo a otro horario del mismo profesional. Con el procedimiento inicial tendría que cancelar el turno y crear otro. Si el nuevo horario se ocupa entre ambas operaciones, el paciente pierde su reserva original.

**RF-04 propuesto.** Recepción podrá reprogramar un turno activo conservando su identificador. Si el destino deja de estar disponible, el paciente conservará íntegramente su reserva original.

## 2. Análisis de impacto de Grijalva

| Elemento | Impacto y decisión técnica |
|---|---|
| Alcance | Se incorpora el cambio de fecha u hora para el mismo profesional. Cambiar de profesional queda fuera de SC-01. |
| Requisitos relacionados | RF-01 permite consultar horarios libres. RF-02 exige una sola reserva activa por horario. RF-03 sigue cubriendo la cancelación voluntaria. |
| Diseño y datos | Se propone confirmar el destino y liberar el origen en una única transacción. El turno conserva su identificador y el historial registra los horarios anterior y nuevo. |
| Riesgo | Dos usuarios podrían solicitar el mismo destino. Se verificará su disponibilidad al confirmar y se aplicará la regla de reserva única. |
| Alternativa evaluada | Mantener la cancelación y la creación manual evita esfuerzo adicional, pero deja a recepción sin garantía de conservar la cita original. |

## 3. Esfuerzo estimado y viabilidad

| Actividad | Responsable | Horas-persona estimadas |
|---|---|---:|
| Precisar RF-04 y sus criterios | Solano | 2 |
| Diseñar e implementar la operación | Grijalva | 4 |
| Preparar y ejecutar las pruebas iniciales | Toapanta | 2 |
| **Total** | | **8** |

Para resolver el ejercicio se supone que quedan ocho horas-persona disponibles dentro del trabajo presupuestado. Bajo ese supuesto se conserva la referencia de 12 semanas y USD 18.000. Sandoval debe contrastar la disponibilidad con el cronograma vigente antes de comprometer el cambio en un proyecto real.

## 4. Decisión y condiciones de aceptación

En la simulación, recepción acepta incorporar RF-04 y Sandoval autoriza planificar las ocho horas estimadas. Solano registra RF-04, Grijalva asume el ajuste técnico y Toapanta verifica los siguientes criterios. La revisión del documento en GitHub queda pendiente.

| Prueba | Situación | Resultado esperado |
|---|---|---|
| CP-04A | Trasladar un turno a un horario libre. | Se ocupa el destino, se libera el origen y se conserva el identificador. El historial registra el traslado. |
| CP-04B | Intentar trasladarlo a un horario ocupado. | Se informa el conflicto. El turno original y la reserva que ocupa el destino conservan sus datos. |
| CP-04C | Dos turnos solicitan simultáneamente el mismo destino libre. | Solo uno se traslada. El otro conserva su horario original. |

## 5. Historial

| Versión | Fecha | Responsable | Descripción | Estado |
|---|---|---|---|---|
| v1.0.0 | 23/11/2026 | Grijalva | Registro de SC-01, análisis de impacto y decisión simulada. | En elaboración |
