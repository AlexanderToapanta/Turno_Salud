# TurnoSalud — Selección del perfil ISO/IEC 29110

## Control documental

| Campo | Información |
|---|---|
| Código | TS-29110-01 |
| Responsable | Grijalva — líder técnico y programador 1 |
| Versión | **v1.0.0** |
| Estado | **En elaboración** |
| Fecha de emisión | 18/11/2026 |
| Aprobador interno | Sandoval — gestor del proyecto |
| Registro de aprobación | Pendiente de revisión por Sandoval |
| Rama de trabajo | `docs/perfil-basico` |

### Historial de versiones

| Versión | Fecha | Responsable | Descripción | Estado |
|---|---|---|---|---|
| v1.0.0 | 18/11/2026 | Grijalva | Selección inicial del Perfil Básico y fundamentación de su aplicación a TurnoSalud. | En elaboración |



---

## 1. Contexto de TurnoSalud

TurnoSalud es el proyecto de una entidad muy pequeña (VSE) situada en Sangolquí que desarrollará una aplicación web de agendamiento de turnos para una clínica privada. El escenario establece **12 semanas de ejecución**, un presupuesto de **USD 18.000** y una condición organizativa decisiva: **durante ese periodo la VSE solo desarrolla este proyecto**. Además, el producto se considera **no crítico para la seguridad**, según la clasificación del ejercicio.

La VSE del caso dispone de seis puestos: gestor del proyecto, líder técnico, analista-diseñador, dos programadores y responsable de pruebas. En el equipo académico, esos seis puestos se distribuyen entre cuatro estudiantes sin alterar las funciones previstas:

| Integrante | Función asignada |
|---|---|
| Sandoval | Gestor del proyecto |
| Grijalva | Líder técnico y programador 1 |
| Solano | Analista-diseñador y programador 2 |
| Toapanta | Responsable de pruebas |

Esta combinación es apropiada para una VSE porque la misma persona puede asumir distintas funciones cuando posee las competencias necesarias. Lo importante no es que exista una persona exclusiva para cada título, sino que estén identificadas las responsabilidades de planificación, decisión técnica, análisis, construcción y verificación.

## 2. Evaluación de los perfiles de ISO/IEC 29110

La serie ISO/IEC 29110 proporciona perfiles que ajustan las prácticas de ingeniería y gestión al contexto de las entidades pequeñas. Para elegir uno se considera principalmente el tipo de organización, su número de proyectos y la complejidad de coordinación que necesita.

| Perfil | Aplicación característica | Evaluación para TurnoSalud |
|---|---|---|
| Entrada | Iniciativas muy pequeñas o emprendimientos en etapas iniciales. | El caso no indica la antigüedad de la VSE ni el esfuerzo total previsto en persona-meses. |
| **Básico** | Un solo equipo que desarrolla un único producto de software. | **Coincide directamente** con la situación establecida. Integra gestión del proyecto e implementación de software. |
| Intermedio | Organizaciones que coordinan varios proyectos simultáneos. | No se justifica incorporar procesos de coordinación multiproyecto cuando existe una sola iniciativa. |
| Avanzado | VSE que necesitan fortalecer la dirección y el crecimiento de toda la organización. | Su alcance organizativo excede lo necesario para planificar el caso. |

Las 12 semanas indican el plazo del proyecto. Para estimar el esfuerzo en persona-meses haría falta conocer la dedicación de cada integrante. La elección del Perfil Básico se apoya en un dato explícito del caso: un solo equipo desarrollará un único producto, la aplicación web de agendamiento de turnos.

## 3. Decisión: Perfil Básico de software

Se selecciona el **Perfil Básico de ISO/IEC 29110** como referencia de gestión e ingeniería para TurnoSalud. Esta elección se sustenta en cuatro argumentos.

**Correspondencia organizativa.** La VSE tiene un tamaño reducido y está concentrada en una sola aplicación. El Perfil Básico fue concebido precisamente para un equipo que desarrolla un único producto de software, por lo que evita procedimientos de coordinación innecesarios entre proyectos.

**Control del trabajo.** Una duración fija de 12 semanas y un presupuesto de USD 18.000 requieren identificar entregables, asignar responsables, ordenar dependencias y establecer puntos de seguimiento. El proceso de Gestión del Proyecto ofrece una estructura para hacerlo sin convertir el ejercicio en una gestión empresarial de gran escala.

**Cobertura técnica.** La aplicación web debe pasar, durante su ejecución futura, por análisis de requisitos, diseño, construcción, integración y pruebas. El proceso de Implementación de Software permite ordenar esas actividades y relacionar sus resultados, reduciendo el riesgo de programar antes de comprender lo que la clínica necesita.

**Compatibilidad con la criticidad declarada.** La presentación señala que la solución no es crítica para la seguridad, condición coherente con el grupo de perfiles genéricos descrito en el material. Esto no significa que se puedan ignorar la confidencialidad de los datos personales, los accesos o la calidad del software; significa únicamente que el caso no está definido como un sistema de seguridad crítica.

Por estas razones, el Perfil Básico ofrece un equilibrio entre disciplina documental y esfuerzo de gestión. La decisión identifica un marco de trabajo apropiado; **no implica certificación ISO ni aprobación del cliente**.

## 4. Procesos que organizan el proyecto

El Perfil Básico establece dos procesos complementarios: **Gestión del Proyecto (GP)** e **Implementación de Software (IS)**. GP determina cómo organizar y controlar el esfuerzo; IS define cómo transformar la necesidad del cliente en un producto de software.

### 4.1. Gestión del Proyecto (GP)

| Actividad | Función dentro de TurnoSalud | Razón de su aplicación |
|---|---|---|
| **GP.1 — Planificación** | Establecer alcance, actividades, responsables, cronograma, recursos y presupuesto. | Permite comprobar desde el inicio que el proyecto previsto puede organizarse dentro de 12 semanas y USD 18.000. |
| GP.2 — Ejecución del plan | Coordinar y registrar el trabajo durante la construcción futura. | Hace posible comparar el avance con lo comprometido. |
| GP.3 — Evaluación y control | Analizar desviaciones y decidir ajustes cuando ocurra la ejecución. | Evita que los retrasos y problemas se acumulen sin seguimiento. |
| GP.4 — Cierre | Formalizar la entrega y la aceptación al concluir el proyecto. | Deja evidencia de lo entregado y del resultado del proyecto. |

Para la entrega académica actual se desarrolla la **planificación GP.1**, apoyada en el enunciado revisado. Las demás actividades aparecen solo para mostrar la secuencia del perfil, sin ejecutarlas anticipadamente.

### 4.2. Implementación de Software (IS)

| Actividad | Contribución esperada al proyecto |
|---|---|
| IS.1 — Inicio | Alinear al equipo con el plan y con las condiciones de ejecución. |
| IS.2 — Análisis de requisitos | Precisar las necesidades de agendamiento, las reglas de disponibilidad y los usuarios de la clínica. |
| IS.3 — Arquitectura y diseño detallado | Definir la estructura de la aplicación y la interacción de sus componentes. |
| IS.4 — Construcción | Implementar las funciones acordadas y verificar componentes. |
| IS.5 — Integración y pruebas | Comprobar que los módulos funcionen juntos y respondan a los criterios definidos. |
| IS.6 — Entrega | Preparar el producto y su documentación para el cliente. |

Estas actividades son relevantes porque explican por qué el plan reserva tiempo para análisis, diseño, desarrollo y pruebas en lugar de dedicar las 12 semanas exclusivamente a programación. **Su ejecución queda fuera de los tres puntos solicitados en esta entrega.**

## 5. Efecto de la selección en los documentos del proyecto

La selección del perfil establece la base metodológica de los demás documentos. El **Enunciado del trabajo** delimita qué problema busca resolver la clínica y distingue los datos conocidos de las decisiones por confirmar. A partir de él, el **Plan del proyecto** determina cómo se emplearán el equipo, el tiempo y el presupuesto. El **Cronograma y recursos** traduce esa planificación en semanas, responsables y dependencias concretas.

La relación es deliberada: primero se determina **cómo se gestionará** el proyecto, después **qué se pretende entregar** y, finalmente, **cómo se organizará el esfuerzo**. Este orden mantiene coherencia entre las decisiones técnicas y las restricciones del caso.

## 6. Conclusión

El **Perfil Básico** es la opción mejor ajustada a TurnoSalud porque responde a una VSE de seis puestos que trabaja en un único proyecto de software no crítico para la seguridad, con plazo y presupuesto definidos. Proporciona las actividades necesarias para planificar y, en una etapa posterior, implementar la aplicación web, sin añadir la complejidad de perfiles destinados a varias iniciativas simultáneas.

