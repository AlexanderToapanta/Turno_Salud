# TurnoSalud — Enunciado del trabajo y análisis de revisión

## Control documental

| Campo | Información |
|---|---|
| Código | TS-29110-02 |
| Responsable | Solano — analista-diseñador y programador 2 |
| Versión | **v1.0.0** |
| Estado | **En elaboración** |
| Fecha de emisión | 18/11/2026 |
| Aprobador interno | Grijalva — líder técnico y programador 1 |
| Rama de trabajo | `docs/enunciado-trabajo` |
| Validación del cliente | No realizada |

### Historial de versiones

| Versión | Fecha | Responsable | Descripción | Estado |
|---|---|---|---|---|
| v1.0.0 | 18/11/2026 | Solano | Formulación del enunciado y análisis de sus límites a partir del caso de clase. | En elaboración |



---

## 1. Situación y necesidad del cliente

Una clínica privada requiere una **aplicación web para el agendamiento de turnos**. El propósito general del sistema es facilitar la organización de citas, la consulta de horarios y la administración de reservas de atención mediante un medio digital. La necesidad central es el **agendamiento**, no el manejo integral de historias clínicas ni la automatización de todas las operaciones de la institución.

El caso no describe cómo funciona actualmente la clínica. Por eso, no corresponde afirmar que sus turnos se gestionan en papel, que existen conflictos frecuentes de horarios o que se han medido demoras de atención. Esas situaciones podrían justificar un sistema de citas en un contexto real, pero **no son hechos confirmados en este ejercicio**. La formulación se limita a la necesidad comunicada: disponer de una aplicación web para gestionar turnos.

El desarrollo sería encargado a una VSE de Sangolquí. La situación fija **12 semanas** y **USD 18.000** como restricciones iniciales, y establece que la VSE dedicará ese periodo a un único proyecto. Estas condiciones orientan el alcance hacia una solución de agendamiento acotada y viable, evitando agregar módulos ajenos al propósito principal.

## 2. Objetivo del trabajo

**Objetivo general.** Desarrollar, dentro de un proyecto planificado de 12 semanas y USD 18.000, una aplicación web que permita organizar el agendamiento de turnos de atención para una clínica privada, con funciones de consulta y administración de reservas definidas posteriormente con el cliente.

Para cumplir ese objetivo se plantea una secuencia lógica: comprender las reglas de la agenda, delimitar las funciones esenciales, definir una solución técnica, construirla y verificar su funcionamiento antes de una eventual entrega. En esta etapa se **revisa y documenta el enunciado**; no se está afirmando que las fases posteriores ya se realizaron.

## 3. Alcance de la solución

El alcance base confirmado por la presentación es **una aplicación web para agendar turnos**. Para que ese objetivo pueda traducirse a una planificación, se propone el siguiente **alcance funcional preliminar**, sujeto a confirmación antes de la implementación:

| Función propuesta | Operación prevista | Justificación de inclusión |
|---|---|---|
| Consulta de disponibilidad | Mostrar horarios potencialmente disponibles para reservar. | Un usuario debe conocer las opciones antes de solicitar un turno. |
| Registro de reservas | Asociar una cita con una fecha, hora y datos mínimos de identificación. | Es el resultado central del proceso de agendamiento. |
| Administración de agenda | Permitir que personal autorizado configure o consulte los espacios de atención. | La disponibilidad necesita una fuente administrable para evitar reservas inconsistentes. |
| Reprogramación y cancelación | Modificar o liberar reservas existentes bajo reglas definidas. | La agenda debe poder responder a cambios sin duplicar turnos. |
| Consulta de turnos | Visualizar las reservas registradas por el perfil correspondiente. | Facilita la operación cotidiana y la comprobación de reservas. |
| Control de acceso | Diferenciar acciones de los usuarios según el rol permitido. | Reduce cambios no autorizados y limita el acceso a información de pacientes. |

Estas funciones son un **modelo inicial de solución**, no una lista de requisitos formalmente aprobados. Su inclusión se basa en la relación directa que guardan con la reserva y administración de turnos; no se agregan funciones complementarias por su posible atractivo comercial.

### Límites del alcance

No se consideran parte del alcance inicial la historia clínica electrónica, las recetas médicas, la facturación, los pagos en línea, el inventario de medicamentos o la integración con aseguradoras y plataformas externas. Su exclusión permite concentrar recursos en el agendamiento y evitar comprometer tiempo o dinero para necesidades que la clínica no ha solicitado expresamente.

La exclusión es **provisional**: indica que esos módulos no se presupuestan en esta versión del enunciado. No representa una decisión contractual tomada por el cliente.

## 4. Restricciones y condicionantes

| Condición | Definición | Implicación sobre el proyecto |
|---|---|---|
| Duración | **12 semanas** | El plan debe distribuir análisis, diseño, construcción, pruebas y preparación de entrega dentro de ese horizonte. |
| Presupuesto | **USD 18.000** | La asignación de esfuerzo y recursos no puede superar el límite del caso. |
| Organización ejecutora | VSE de seis puestos | El trabajo debe coordinarse con una estructura pequeña y responsabilidades claras. |
| Número de proyectos | Uno durante el periodo | Se utiliza el Perfil Básico y no se presupuesta trabajo simultáneo en otros proyectos. |
| Plataforma solicitada | Web | La solución se concibe para utilizarse mediante un navegador, sin comprometer una aplicación móvil nativa. |
| Clasificación del caso | Producto no crítico para la seguridad | Se aplica el Perfil Básico genérico, sin interpretar esta clasificación como permiso para descuidar privacidad o acceso. |

Las condiciones anteriores provienen directamente del escenario, salvo las consecuencias de diseño y gestión, que son decisiones razonadas del equipo.

## 5. Usuarios y reglas operativas por definir

Una aplicación de turnos depende de reglas propias de cada clínica. El enunciado no señala cuántos profesionales atienden, si existen especialidades, si los pacientes reservan por sí mismos, cuánto dura cada consulta ni con qué anticipación se puede cancelar una reserva. Tampoco determina qué información personal es indispensable.

Para mantener un alcance técnicamente viable, la planificación supone una **agenda administrada por personal autorizado** y reservas identificables por fecha y hora. Antes de convertir esa hipótesis en requisitos definitivos, sería necesario definir al menos los siguientes asuntos:

| Aspecto no especificado | Incidencia sobre el diseño y la estimación |
|---|---|
| Número de agendas y profesionales | Determina la complejidad de disponibilidad y asignación de turnos. |
| Perfiles de usuario | Define permisos, interfaces y responsabilidades. |
| Duración y calendario de atención | Determina las reglas para generar y bloquear horarios. |
| Política de cancelación y reprogramación | Determina cuándo se permite modificar una reserva. |
| Datos necesarios para identificar reservas | Influye en formularios, privacidad y almacenamiento. |
| Responsable de aceptación por la clínica | Permite establecer quién evaluará el resultado en etapas posteriores. |

**Resultado de la revisión:** el enunciado resulta suficiente como punto de partida para una **planificación preliminar**, pero no para fijar especificaciones detalladas de software ni declarar aceptación del cliente. La distinción evita presentar supuestos del equipo como acuerdos contractuales.

## 6. Entregables del proyecto planificado

En una ejecución completa se esperaría obtener un conjunto ordenado de productos que permita comprender, construir, comprobar y entregar el software:

| Etapa prevista | Entregable | Utilidad |
|---|---|---|
| Planificación | Plan del proyecto y cronograma | Relacionan alcance, plazo, recursos y responsables. |
| Análisis | Especificación de requisitos | Traduce las necesidades de la clínica a funciones verificables. |
| Diseño | Diseño de arquitectura, datos e interfaces | Establece la organización de la solución antes de programar. |
| Construcción | Componentes de la aplicación web | Materializan las funciones aprobadas. |
| Integración y pruebas | Evidencia de funcionamiento | Permite identificar defectos y comprobar el comportamiento esperado. |
| Entrega | Producto y documentación de uso | Facilitan la utilización y administración posterior del sistema. |

Esta tabla **describe entregables previstos para el proyecto de 12 semanas**; no significa que se deban producir ahora los productos posteriores a la planificación. La entrega académica vigente contiene la selección del perfil, este enunciado y el plan con su cronograma.

## 7. Resultado del análisis del enunciado

La revisión identifica que el escenario es coherente a nivel de propósito, restricciones y tipo de solución, pero deja abiertas las reglas específicas de la clínica. En consecuencia, se adopta una interpretación **restringida al agendamiento web**, con funciones auxiliares mínimas que explican cómo podría operar una reserva.

Esta decisión protege la viabilidad del proyecto: fija una base para estimar tiempo y recursos sin comprometer módulos no solicitados. También mantiene trazabilidad entre el problema expresado por la clínica y el plan de trabajo. Cualquier definición funcional detallada requeriría una validación posterior, separada de la revisión del enunciado efectuada aquí.

La revisión interna de Grijalva permitirá comprobar la coherencia técnica del planteamiento antes de integrar esta versión al repositorio principal. **Hasta que esa revisión ocurra, el estado sigue siendo `En elaboración`.**
