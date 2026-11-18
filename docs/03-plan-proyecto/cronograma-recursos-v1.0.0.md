# TurnoSalud — Cronograma y asignación de recursos

## Control documental

| Campo | Información |
|---|---|
| Código | TS-29110-04 |
| Responsable | Toapanta — responsable de pruebas |
| Versión | **v1.0.0** |
| Estado | **En elaboración** |
| Fecha de emisión | 18/11/2026 |
| Aprobador interno | Sandoval — gestor del proyecto |
| Rama de trabajo | `docs/cronograma-recursos` |
| Documento principal | [`plan-proyecto.md`](plan-proyecto.md) |

### Historial de versiones

| Versión | Fecha | Responsable | Descripción | Estado |
|---|---|---|---|---|
| v1.0.0 | 18/11/2026 | Toapanta | Distribución inicial de semanas, dependencias, responsables y recursos de TurnoSalud. | En elaboración |


---

## 1. Criterio para organizar el cronograma

El proyecto TurnoSalud dispone de **12 semanas** y un presupuesto de **USD 18.000**. El cronograma transforma ese plazo en una secuencia de trabajos y resultados, utilizando como referencia el **Plan del proyecto** y las actividades del Perfil Básico de ISO/IEC 29110.

Se utilizan **semanas relativas (S1 a S12)** en lugar de fechas específicas porque el caso no informa un día contractual de inicio. Esta decisión evita inventar fechas y permite visualizar el orden y la duración de las fases.

Se reserva tiempo para comprender las reglas de agendamiento, diseñar, construir, integrar y verificar el sistema. La programación no ocupa todo el calendario: en una aplicación que administra reservas, también es necesario asegurar que los horarios, usuarios y cambios de turnos funcionen de forma consistente.

## 2. Calendario de 12 semanas

| Semana | Actividad planificada | Responsable(s) | Resultado previsto | Razón de la secuencia |
|---|---|---|---|---|
| **S1** | Inicio, revisión del enunciado, selección de perfil y plan base. | Sandoval, Grijalva, Solano, Toapanta | Plan y organización inicial. | Se establecen las condiciones del trabajo antes de desarrollar. |
| **S2** | Identificación de usuarios, necesidades y operaciones de reserva. | Solano, con Grijalva | Alcance funcional detallado en preparación. | Las funciones deben estar entendidas antes del diseño. |
| **S3** | Precisión de disponibilidad, reprogramación y reglas operativas. | Solano, con Sandoval | Requisitos definidos para la siguiente fase. | Las reglas de agenda afectan directamente al modelo de datos. |
| **S4** | Propuesta de arquitectura y estructura de información. | Grijalva, con Solano | Diseño general del sistema. | La arquitectura organiza las responsabilidades de los componentes. |
| **S5** | Diseño de interfaces y operaciones principales. | Solano y Grijalva | Diseño preparado para construir. | Las interacciones se definen antes de implementarlas. |
| **S6** | Construcción inicial de los componentes de agenda. | Grijalva | Primer conjunto de componentes. | Se comienza por la base de disponibilidad y reservas. |
| **S7** | Implementación de registro y administración de turnos. | Grijalva y Solano | Funciones de agendamiento conectadas. | Se desarrolla el núcleo que materializa el objetivo del cliente. |
| **S8** | Construcción de interfaces y consolidación funcional. | Solano, con Grijalva | Funciones principales disponibles. | Se completa una base para integración y pruebas. |
| **S9** | Integración de componentes y preparación de verificaciones. | Grijalva, Solano, Toapanta | Sistema integrado de referencia. | Se comprueba la interacción entre módulos. |
| **S10** | Pruebas sobre reserva, consulta y modificación de turnos. | Toapanta, con apoyo del equipo | Resultados de verificación. | Se detectan errores antes de la preparación de entrega. |
| **S11** | Correcciones y documentación operativa. | Grijalva, Solano, Toapanta | Versión candidata y documentación. | Se aprovechan los hallazgos de las verificaciones. |
| **S12** | Preparación de la entrega prevista. | Sandoval, con el equipo | Paquete final de entrega. | Se organiza una salida formal del trabajo desarrollado. |

**Alcance de la entrega académica:** este calendario se **planifica**, pero no se ejecuta en el ejercicio actual. Solo se presentan la selección del perfil, la revisión del enunciado y el Plan del proyecto. Las semanas 2–12 representan trabajo eventual de una ejecución completa.

## 3. Distribución por fases

| Fase | Intervalo | Semanas asignadas | Resultado que inicia la fase siguiente |
|---|---|---:|---|
| Inicio y planificación | S1 | 1 | Plan base definido. |
| Requisitos | S2–S3 | 2 | Reglas y funciones suficientemente descritas para diseñar. |
| Arquitectura y diseño | S4–S5 | 2 | Estructura técnica e interfaces previstas. |
| Construcción | S6–S8 | 3 | Funciones principales implementadas. |
| Integración y pruebas | S9–S10 | 2 | Comportamiento conjunto comprobado. |
| Ajustes y preparación de entrega | S11–S12 | 2 | Producto y documentación preparados. |
| **Total** | **S1–S12** | **12** | |

La construcción recibe tres semanas continuas, pero no se ubica al inicio. Este reparto disminuye el riesgo de desarrollar comportamientos que luego deban modificarse por haber omitido el análisis. Las pruebas cuentan con un bloque específico, además de las comprobaciones que pueden realizarse durante la implementación.

## 4. Dependencias y ruta de trabajo

El calendario sigue una cadena principal de dependencias: **planificación → requisitos → diseño → construcción → integración y pruebas → preparación de entrega**. Cada fase produce información o componentes necesarios para la siguiente.

El mayor riesgo para esta secuencia es la definición tardía de las reglas de la agenda. Si se determina demasiado tarde que los turnos tienen distintas duraciones, varios profesionales o restricciones de disponibilidad, podrían verse afectados tanto el diseño de datos como los formularios y la lógica de reservas. Por ello se asignan las semanas 2 y 3 a entender esas condiciones antes de construir.

Los puntos de referencia se concentran en las semanas **1, 3, 5, 8, 10 y 12**. Son hitos planificados, no fechas de entregables ya aprobados. Sirven para detectar con anticipación si el proyecto deja de avanzar al ritmo esperado.

## 5. Asignación de recursos humanos

En el caso se describen **seis puestos**, representados académicamente por **cuatro integrantes**. La asignación considera quién posee la responsabilidad principal y en qué momentos se necesita su participación.

| Integrante | Roles | Participación principal | Fundamento |
|---|---|---|---|
| **Sandoval** | Gestor del proyecto | S1–S12: planificación, coordinación, control y preparación de entrega. | La gestión requiere continuidad durante todo el proyecto. |
| **Grijalva** | Líder técnico y programador 1 | S1–S10: orientación técnica, diseño, desarrollo e integración; apoyo posterior cuando sea necesario. | La coherencia técnica debe sostenerse desde la planificación hasta la integración. |
| **Solano** | Analista-diseñador y programador 2 | S1–S11: enunciado, requisitos, interfaces, implementación y ajustes. | Conecta lo solicitado por el cliente con el diseño y la construcción. |
| **Toapanta** | Responsable de pruebas | S1: cronograma y previsiones de calidad; S5–S11: criterios de prueba, integración, verificación y revisión de ajustes. | Planificar la calidad desde el principio evita descubrir al final que faltó tiempo para probar. |

Las participaciones se describen por periodos, **sin asignar horas individuales ficticias**: la diapositiva no proporciona jornadas ni disponibilidad laboral. La intensidad real de trabajo dependería del desglose posterior de tareas.

En la elaboración del ejercicio se mantienen los siguientes autores: **Grijalva** para el Perfil Básico, **Solano** para el Enunciado del trabajo, **Sandoval** para el Plan del proyecto y **Toapanta** para este cronograma. Esto distribuye la documentación de forma equilibrada y permite integrar cuatro contribuciones independientes en GitHub.

## 6. Recursos técnicos y financieros

El equipo utiliza **Markdown y GitHub** para organizar los cuatro documentos iniciales. Git permite controlar versiones; las ramas separan modificaciones individuales; los Pull Requests ofrecen un punto de revisión antes de integrar el trabajo. Estas herramientas resultan proporcionales a una VSE porque permiten rastreabilidad sin exigir una plataforma de gestión compleja.

Para el desarrollo futuro se prevé la necesidad de un entorno web, una solución para almacenar reservas, una herramienta de diseño y un entorno de pruebas. Ninguna tecnología específica se da por aprobada: el caso no presenta suficientes requisitos para escoger justificadamente un framework o proveedor.

El presupuesto se conserva en **USD 18.000**, conforme al desglose del [`plan-proyecto.md`](plan-proyecto.md). La mayor porción se reserva a construcción, pero el análisis, el diseño y las pruebas cuentan con partidas propias porque condicionan la utilidad y la calidad del producto. También se incorpora una contingencia de USD 1.200 dentro del total, no como un gasto adicional.

## 7. Seguimiento previsto

Sandoval coordinaría una revisión semanal del avance respecto del calendario. Cada responsable comunicaría los productos terminados, las dependencias pendientes y los impedimentos que afecten la siguiente semana. La información podría registrarse en GitHub Issues o en un tablero sencillo vinculado al repositorio.

El criterio para considerar completada una actividad sería disponer del resultado previsto, no simplemente haber invertido tiempo en ella. Por ejemplo, la fase de diseño se evaluaría con un diseño preparado para orientar la construcción; la fase de pruebas, con evidencia de las verificaciones realizadas. Este enfoque hace que el seguimiento se centre en productos comprobables y sea coherente con ISO/IEC 29110.

El mecanismo está **definido como parte del plan**. Todavía no existen mediciones de avance, incidencias reales, resultados de pruebas ni registros de retrabajo, porque la ejecución del proyecto no forma parte de los tres puntos solicitados.

## 8. Conclusión

El cronograma organiza TurnoSalud en **seis fases que suman exactamente 12 semanas**. La secuencia y la asignación de recursos priorizan comprender las reglas de agenda antes de programar y reservar un periodo explícito para integración y pruebas. De esta manera, el tiempo y el personal se distribuyen de forma coherente con el alcance preliminar y con el presupuesto de referencia.


