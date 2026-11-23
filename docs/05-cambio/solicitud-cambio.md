# 5. Gestión de la solicitud de cambio SC-01

| Documento | Autoría | Versión | Fecha |
|---|---|---|---|
| TS-SC-01 | Grijalva | v1.0.0 | 23/11/2026 |

## Solicitud y origen

**Cambio solicitado:** reprogramar un turno activo en la agenda del mismo profesional. En la simulación, recepción identifica un problema con el procedimiento inicial: si cancela una reserva antes de confirmar el nuevo horario, otro usuario podría ocupar ese horario y el paciente perdería su cita original.

**Requisito incorporado (RF-04).** Recepción podrá cambiar la fecha o la hora de un turno activo. Si el destino está disponible, el turno conservará su identificador y quedará asociado al nuevo horario. Si el traslado falla, el paciente conservará su reserva original.

## Impacto sobre el proyecto

| Elemento | Efecto del cambio |
|---|---|
| Alcance | Se añade la reprogramación para el mismo profesional. La cancelación voluntaria mantiene las condiciones de RF-03. |
| Agenda e historial | Se comprueba la disponibilidad al confirmar. La asignación del destino, la liberación del origen y el registro del traslado se completan en una sola transacción. |
| Riesgo | Dos usuarios podrían elegir el mismo destino libre. La regla de reserva única de RF-02 debe mantenerse incluso si ambas solicitudes llegan a la vez. |
| Esfuerzo estimado | 2 horas-persona para requisitos y criterios, 4 para diseño y construcción y 2 para pruebas iniciales. Total: **8 horas-persona**. |
| Plazo y presupuesto | Para decidir el cambio se suponen ocho horas disponibles dentro del plan de 12 semanas y USD 18.000. Con esa capacidad, la estimación inicial mantiene el plazo y el presupuesto previstos. |

## Decisión

En el caso simulado se acepta SC-01. La alternativa de cancelar y crear una cita por separado resulta insuficiente porque podría dejar al paciente sin ninguna de las dos reservas. RF-04 amplía los [requisitos iniciales](../04-validacion/validacion-requisitos.md) y queda sujeto a los tres criterios siguientes.

| Prueba | Situación | Criterio de aceptación |
|---|---|---|
| CP-04A | El destino está libre. | El turno conserva su identificador, ocupa el destino y libera el origen. El historial registra ambos horarios. |
| CP-04B | El destino ya está ocupado. | La aplicación informa del conflicto. La reserva del paciente y la que ocupa el destino permanecen en sus horarios originales. |
| CP-04C | Dos turnos solicitan el mismo destino libre. | Un solo turno ocupa el destino. El otro conserva su horario inicial y su usuario recibe el aviso de indisponibilidad. |
