# TurnoSalud — Plan del proyecto

## Control documental

| Campo | Información |
|---|---|
| Código | TS-29110-03 |
| Responsable | Sandoval — gestor del proyecto |
| Versión | **v1.0.0** |
| Estado | **En elaboración** |
| Fecha de emisión | 18/11/2026 |
| Aprobador interno | Grijalva — líder técnico y programador 1 |
| Rama de trabajo | `docs/plan-proyecto` |
| Documento complementario | [`cronograma-recursos.md`](cronograma-recursos.md) |

### Historial de versiones

| Versión | Fecha | Responsable | Descripción | Estado |
|---|---|---|---|---|
| v1.0.0 | 18/11/2026 | Sandoval | Planificación inicial del alcance, presupuesto, recursos, hitos y coordinación del proyecto. | En elaboración |
 v1.0.0 | 18/11/2026 | Grijalva (líder técnico) | Revisión y aprobación interna del Plan del proyecto elaborado por Sandoval. | Aprobado |



---

## 1. Fundamentación del plan

TurnoSalud consiste en el desarrollo previsto de una **aplicación web de agendamiento de turnos para una clínica privada**, a cargo de una VSE de Sangolquí. El caso fija **12 semanas** y un presupuesto total de **USD 18.000**, y aclara que la organización trabajará exclusivamente en este proyecto durante ese periodo.

Se adopta el **Perfil Básico de ISO/IEC 29110** porque corresponde a una entidad pequeña que ejecuta un solo proyecto. El plan aplica la actividad **GP.1 — Planificación**: ordena el trabajo, asigna responsables y establece referencias contra las que se podría evaluar el avance cuando comience la ejecución.

La base del plan es el [`enunciado-trabajo.md`](../02-enunciado-trabajo/enunciado-trabajo.md). Dado que el escenario no contiene requisitos detallados confirmados por la clínica, las funcionalidades y estimaciones se consideran **propuestas iniciales**. La planificación no reemplaza una futura validación de requisitos.

## 2. Objetivo y alcance del proyecto

El objetivo es organizar el desarrollo de una plataforma web orientada a **consultar disponibilidad y gestionar reservas de turnos**. Se plantea como núcleo funcional la consulta de horarios, el registro de citas, la administración de agenda, la visualización de reservas y la modificación o cancelación de turnos bajo reglas de negocio que deberán definirse.

Se limita el alcance a funciones directamente relacionadas con la agenda porque la presentación no exige un sistema de gestión clínica integral. Por ello, no se presupuestan módulos de historia clínica, facturación, farmacia o integraciones con aseguradoras. Esta reducción disminuye la dispersión del esfuerzo y permite una planificación compatible con el plazo y el presupuesto.

La solución se planifica como **web**, tal como especifica el caso. No se seleccionan aún framework, motor de base de datos ni proveedor de infraestructura, pues esa elección debe justificarse con requisitos y restricciones técnicas que todavía no están disponibles.

## 3. Organización del equipo

La situación original contempla seis puestos. Para realizar el trabajo académico, cuatro integrantes asumen esas funciones:

| Integrante | Roles | Responsabilidad en la organización del proyecto |
|---|---|---|
| **Sandoval** | Gestor del proyecto | Coordinar actividades, controlar plazo y presupuesto, organizar entregables y mantener el plan. |
| **Grijalva** | Líder técnico y programador 1 | Definir criterios técnicos, orientar el diseño y participar en la construcción prevista. |
| **Solano** | Analista-diseñador y programador 2 | Delimitar alcance, analizar necesidades, diseñar la solución y desarrollar componentes previstos. |
| **Toapanta** | Responsable de pruebas | Considerar desde la planificación las verificaciones necesarias y coordinar la asignación temporal de recursos y pruebas futuras. |

La división es funcional: Sandoval responde por la gestión general, Grijalva por la coherencia técnica, Solano por conectar la necesidad del cliente con la solución y Toapanta por asegurar que se reserve tiempo para comprobarla. La asignación del cronograma a Toapanta distribuye el trabajo documental sin modificar su rol de responsable de pruebas.

## 4. Estrategia de ejecución y fases

Se propone un **desarrollo incremental con controles de avance**. La aplicación se estructuraría en funciones de agendamiento que puedan analizarse, construirse y comprobarse por etapas. Este enfoque es adecuado para un producto cuyo detalle aún debe precisarse, ya que permite incorporar lo aprendido en el análisis antes de comprometer toda la construcción.

El plan mantiene, a la vez, la secuencia de actividades de **Implementación de Software (IS)** descrita en el Perfil Básico: inicio, requisitos, diseño, construcción, integración/pruebas y entrega. Las fases se distribuyen así:

| Fase prevista | Semanas | Trabajo y resultado esperados | Motivo de ubicación |
|---|---|---|---|
| **Inicio y planificación** | **1** | Organizar equipo, revisar enunciado y establecer plan base. | Alinear alcance, responsabilidades y restricciones antes de consumir recursos de desarrollo. |
| **Análisis de requisitos** | **2–3** | Precisar actores, reglas de agenda y funciones a implementar. | Evitar diseñar sobre supuestos no examinados. |
| **Diseño de la solución** | **4–5** | Definir arquitectura, estructura de datos e interfaces. | Reducir incertidumbre técnica antes de programar. |
| **Construcción** | **6–8** | Desarrollar los componentes de reservas y administración. | Concentrar el mayor esfuerzo en el núcleo funcional. |
| **Integración y pruebas** | **9–10** | Integrar componentes y verificar flujos principales. | Detectar problemas entre módulos con tiempo para corregirlos. |
| **Ajustes y preparación de entrega** | **11–12** | Corregir defectos detectados y preparar documentación y entrega. | Evitar que el proyecto termine inmediatamente al finalizar la programación. |

Las 12 semanas constituyen el **horizonte planificado del caso**, no un registro de ejecución. La entrega de clase actual solo documenta la elección del perfil, la revisión del enunciado y la elaboración de este plan.

## 5. Hitos y resultados esperados

| Hito | Semana prevista | Resultado que permitirá evaluar el avance |
|---|---:|---|
| H1 — Plan base | 1 | Alcance provisional, equipo, estimaciones y cronograma documentados. |
| H2 — Requisitos definidos | 3 | Funciones y reglas descritas para orientar el diseño. |
| H3 — Diseño disponible | 5 | Solución técnica y estructura de datos descritas. |
| H4 — Construcción principal | 8 | Componentes esenciales desarrollados. |
| H5 — Integración comprobada | 10 | Resultado de pruebas sobre los flujos principales. |
| H6 — Preparación de entrega | 12 | Versión preparada para la revisión final y documentación asociada. |

Los hitos separan resultados verificables en lugar de medir únicamente tiempo transcurrido. De esa manera, un avance puede relacionarse con un producto concreto: disponer de un diseño antes de construir es más informativo que afirmar que han transcurrido cinco semanas.

## 6. Presupuesto propuesto

El presupuesto máximo es un **dato del ejercicio**; su distribución por rubros es una **estimación elaborada para este plan**, no una cotización acordada con la clínica.

| Rubro | Monto (USD) | Justificación |
|---|---:|---|
| Gestión y coordinación | 2.600 | Planificación, coordinación del equipo y control de avance. |
| Análisis de requisitos | 2.400 | Identificación de reglas de agenda y definición del alcance funcional. |
| Arquitectura y diseño | 2.000 | Definición de módulos, datos e interfaces antes de implementar. |
| Construcción del software | 7.000 | Desarrollo de las funciones principales de la aplicación web. |
| Integración y pruebas | 2.200 | Verificación de las operaciones de reserva y funcionamiento conjunto. |
| Infraestructura y herramientas | 600 | Necesidades técnicas de repositorio, entornos y eventual alojamiento. |
| Reserva de contingencia | 1.200 | Margen para imprevistos dentro del límite autorizado del caso. |
| **Total** | **18.000** | **Se respeta el presupuesto de referencia.** |

La construcción representa la mayor partida porque allí se materializa la funcionalidad. Sin embargo, se asignan recursos diferenciados al análisis y las pruebas: omitirlos produciría un presupuesto aparentemente más barato, pero sin suficiente capacidad para definir y verificar lo que se desarrolla. La **reserva de contingencia está incluida** en los USD 18.000; no incrementa el total disponible.

## 7. Recursos y mecanismos de trabajo

En recursos humanos se prevé la participación de los cuatro integrantes que representan los seis puestos del caso. La dedicación exacta por persona no se cuantifica en horas porque el escenario no proporciona jornadas laborales ni tarifas. Por ese motivo, el presupuesto se distribuye por actividades y no se presenta como una nómina salarial cerrada.

Para la gestión documental se utilizarán **Git, GitHub y Markdown**. Cada autor mantendrá su trabajo en una rama independiente; antes de integrarlo a `main`, otro integrante revisará el contenido mediante un Pull Request. Esta práctica permite identificar quién realizó un cambio y conservar las decisiones de revisión. Durante una eventual construcción, podrían agregarse herramientas de seguimiento, modelado, desarrollo y pruebas, elegidas según las necesidades técnicas definidas.

Los criterios de aprobación interna de los documentos ya están definidos en el [`README.md`](../../README.md). Una aprobación del equipo **no equivale** a la aceptación de requisitos por parte de la clínica.

## 8. Seguimiento del proyecto previsto

El control se organizaría en revisiones semanales coordinadas por Sandoval. En cada revisión se compararía el trabajo previsto con el resultado alcanzado, se identificarían bloqueos y se actualizarían las prioridades de la etapa. El cronograma funcionaría como referencia común: si una tarea previa se retrasa, el efecto sobre sus dependencias debe poder observarse antes de la semana de entrega.

Se propone registrar actividades en GitHub Issues o en un tablero del proyecto y utilizar Pull Requests como evidencia de revisión de artefactos. Al llegar a cada hito, se comprobaría que el entregable relacionado existe y está en condiciones de pasar a la siguiente fase. Esta es una **estrategia de control definida durante la planificación**; no constituye un reporte de avance ejecutado ni una medición de retrabajo.

## 9. Riesgos iniciales y decisiones preventivas

| Riesgo | Consecuencia probable | Medida prevista y justificación |
|---|---|---|
| Reglas de agenda incompletas | Rehacer interfaces o lógica de reservas. | Concentrar las semanas 2–3 en precisar las reglas antes del diseño. |
| Estimaciones demasiado optimistas | Pérdida de margen al acercarse la entrega. | Usar hitos intermedios y una reserva presupuestaria de contingencia. |
| Concentración de responsabilidades | Cuellos de botella en las decisiones o revisiones. | Asignar un responsable por producto y revisores distintos de los autores. |
| Problemas de integración | Funciones correctas de forma aislada que fallen en conjunto. | Reservar expresamente las semanas 9–10 para integración y pruebas. |
| Definición tardía de permisos y datos | Modificaciones importantes en el diseño. | Considerar usuarios, acceso y datos mínimos desde el análisis inicial. |

Estas previsiones no suponen que los riesgos ya ocurrieron. Son hipótesis razonables que ayudan a justificar el orden de actividades y la asignación de recursos.

## 10. Coherencia con el enunciado y decisión de planificación

El plan conserva exactamente las restricciones conocidas: **proyecto web, clínica privada, 12 semanas, USD 18.000 y una VSE dedicada a un solo proyecto**. Las funciones candidatas proceden del enunciado elaborado por Solano, mientras que el detalle de dependencias y responsables se desarrolla en el anexo de Toapanta.

La decisión central es **priorizar el agendamiento de turnos**, establecer entregables intermedios y reservar tiempo para integración y pruebas. De este modo, el proyecto se organiza para alcanzar un objetivo limitado y verificable, en lugar de intentar cubrir toda la operación clínica con información insuficiente.

