# TurnoSalud — Medición del retrabajo

| Control documental | Detalle |
|---|---|
| Código | TS-MED-01 |
| Versión y fecha | v1.0.0 · 23/11/2026 |
| Responsable | Toapanta, responsable de pruebas |
| Revisor interno | Grijalva, líder técnico |
| Estado | En elaboración |
| Aprobación interna | Pendiente de revisión en GitHub |
| Referencia | [Solicitud SC-01 y pruebas de RF-04](../05-cambio/solicitud-cambio.md) |

## 1. Periodo y definición

Se analiza un bloque simulado de 40 horas-persona dedicado a requisitos, trabajo técnico y pruebas. En este ejercicio se contabilizan como retrabajo las horas empleadas en corregir un incumplimiento y repetir las pruebas afectadas. La primera implementación de RF-04 se registra como trabajo del cambio aprobado.

Las horas y los resultados siguientes son datos académicos simulados. La medición se limita al bloque analizado y no representa las 12 semanas completas del proyecto.

## 2. Registro del esfuerzo

| Trabajo realizado en la simulación | Horas planificadas ejecutadas | Horas de retrabajo | Total |
|---|---:|---:|---:|
| Trabajo inicial y verificaciones de RF-01 a RF-03 | 28 | 0 | 28 |
| Incorporación de RF-04 y pruebas iniciales de SC-01 | 8 | 0 | 8 |
| Corrección técnica del defecto D-01 por Grijalva | 0 | 3 | 3 |
| Repetición de las pruebas afectadas por Toapanta | 0 | 1 | 1 |
| **Total de horas-persona** | **36** | **4** | **40** |

## 3. Defecto que originó el retrabajo

| Campo | Registro simulado D-01 |
|---|---|
| Prueba de detección | CP-04B, reprogramación con destino ocupado. |
| Resultado esperado | Conservar la reserva original y avisar del conflicto. |
| Resultado observado en el escenario | El sistema informó del conflicto, pero el horario original quedó libre. |
| Corrección | Grijalva agrupó la actualización del turno y la liberación del horario original en una misma transacción. |
| Comprobación posterior | CP-04B conservó la reserva original. Se repitieron CP-04A y CP-04C para comprobar el traslado válido y la concurrencia. |
| Resultado final del escenario | Las tres comprobaciones cumplieron sus criterios. D-01 quedó cerrado. |

## 4. Cálculo e interpretación

**Porcentaje de retrabajo = horas de retrabajo / horas totales ejecutadas × 100.**

**Resultado = (3 + 1) / 40 × 100 = 10 %.**

De cada diez horas del bloque analizado, una se dedicó a corregir y volver a probar. Las ocho horas de SC-01 corresponden a incorporar una capacidad nueva; las cuatro horas de D-01 corresponden a corregir su comportamiento. El caso no proporciona un umbral para calificar el porcentaje como aceptable o excesivo.

**Acción de mejora.** Antes de construir otra operación que modifique reservas, Grijalva y Toapanta definirán juntos qué datos deben conservarse cuando la operación falla. La revisión incluirá al menos un conflicto de horario y dos solicitudes simultáneas.

## 5. Historial

| Versión | Fecha | Responsable | Descripción | Estado |
|---|---|---|---|---|
| v1.0.0 | 23/11/2026 | Toapanta | Primera medición simulada y registro del defecto D-01. | En elaboración |
