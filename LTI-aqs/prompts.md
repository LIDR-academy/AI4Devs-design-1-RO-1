**Agente IA usado**: Chat GPT (Gratuito)

**Prompt 1**: En modo razonamiento

Esta tarea debería tener el punto de vista de un product manager.
Se necesita hacer el diseño y documentación del sistema de sofware siguiendo las siguientes fases:
1. Investigación y análisis
2. Casos de Uso
3. Modelado de datos
4. Diseño de alto nivel

El sistema es para una startup llamada LTI, que quiere desarrollar el ATS del futuro. Se adjunta imágen con los puntos principales de un ATS.

Todavía no hay nada creado, así que hay que definir las funcionalidades clave que harán brillar a LTI por encima de los competidores:
* aumentar la eficiencia para los departamentos de HR
* mejorar la colaboración en tiempo real entre reclutadores y managers, automatizaciones
* asistencia de IA en diversas tareas

Hay que hacer brainstorming, investigar cuáles pueden ser las claves del éxito, y dejarlo plasmado para el resto del equipo.

La primera versión del sistema debe contar con:
* Descripción breve del software LTI, valor añadido y ventajas competitivas. Explicación de las funciones principales. Añadir un diagrama Lean Canvas para entender el modelo de negocio.
* Descripción de los 3 casos de uso principales, con el diagrama asociado a cada uno
* Modelo de datos que cubra entidades, atributos (nombre y tipo) y relaciones
* Diseño del sistema a alto nivel, tanto explicado como diagrama adjunto
* Diagrama C4 que llegue en profundidad a uno de los componentes del sistema

Usando Metaprompting, define los prompt adecuados, permitan poder realizar en conjunto con la IA y una persona, el plan de trabajo para lograr esta tarea. Hazme las preguntas que consideres que importantes, para aclarar ideas y ver que puntos fueron omitidos y sería importante incluir.

**Respuesta 1**:

A continuación encontrarás una propuesta de Meta-prompts organizados por fases, que te ayudarán a colaborar con la IA y con tu equipo humano para generar cada artefacto solicitado. Al final incluyo también una serie de preguntas de aclaración que sugiero hacer al inicio del proyecto para no omitir ningún punto crítico.

1. Investigación y análisis
* Prompt IA (mercado y competencia)

> “Eres un Product Manager que está analizando el mercado de Applicant Tracking Systems (ATS). Describe las tendencias actuales, principales retos de los departamentos de RR.HH., y analiza 5 competidores líderes (por ejemplo Greenhouse, Lever, SmartRecruiters, etc.), señalando sus fortalezas y debilidades.”

* Prompt IA (usuarios y necesidades)

> “Identifica y perfila a los stakeholders clave de nuestro ATS (reclutadores, hiring managers, candidatos, TI…). Para cada uno, resume sus pains & gains y prioriza sus necesidades más críticas.”

* Prompt IA (valor diferencial LTI)

> “Con base en la investigación previa, genera una propuesta de valor para LTI: ¿qué funcionalidades, flujos y asistencias de IA pueden convertirlo en el ‘ATS del futuro’? Enumera al menos 3 pilares diferenciales.”

2. Casos de Uso
* Prompt IA (selección de casos)

> “Propón los 3 casos de uso principales para la primera versión de LTI (por ejemplo: creación y seguimiento de ofertas, colaboración en selección, onboarding preliminar). Para cada uno, escribe un título, actor(es), precondición, flujo principal y flujo alternativo.”

* Prompt IA (diagramas UML)

> “A partir de los casos de uso definidos, genera un diagrama de casos de uso UML (lista de actores y relaciones con cada caso) y describe cómo se visualizaría gráficamente.”

3. Modelado de datos
* Prompt IA (entidades y atributos)

> “Diseña un modelo lógico de datos para LTI: define al menos 8–10 entidades (Job, Candidate, Application, User, Interview, Feedback, AutomationRule, etc.), con sus atributos principales (nombre y tipo) y relaciones entre ellas (1-n, n-m).”

* Prompt IA (diagrama ER)

> “Convierte el modelo lógico en un diagrama Entidad-Relación describiendo llaves primarias, foráneas y cardinalidades.”

4. Diseño de alto nivel
* Prompt IA (arquitectura y componentes)

> “Escribe una descripción narrativa de la arquitectura de LTI: front-end, back-end, bases de datos, servicios de IA, colas de eventos, integraciones con proveedores de correo y HRIS. Luego elabora un diagrama de alto nivel (tipo caja-y-líneas) que lo represente.”

* Prompt IA (diagrama C4 – componente)

> “Profundiza en uno de los componentes críticos (por ejemplo, el módulo de ‘Asistencia de IA para criba de CV’): describe sus subcomponentes, interfaces, tecnologías sugeridas y muestra un diagrama C4 (nivel 3) de ese módulo.”

# Plan de trabajo colaborativo
1. Kick-off interno
    * Reunión de 1h con stakeholders.
    * Revisar prompts y confirmar objetivos.

2. Sprints de IA + revisión humana
    * Sprint 1 (2 días): Investigación de mercado y propuesta de valor.
    * Sprint 2 (2 días): Redacción de casos de uso + diagramas.
    * Sprint 3 (2 días): Modelado de datos y diagrama ER.
    * Sprint 4 (2 días): Arquitectura y diagramas C4.
3. Revisión final y documentación
    * Consolidar artefactos en un único repositorio (Docs & Confluence).
    * Feedback de TI, RR.HH. y Dirección.

# Preguntas de aclaración iniciales
1. Alcance y prioridades
    * ¿Qué módulos son must-have en MVP y cuáles pueden dejarse para versiones posteriores?
    * ¿Hay requerimientos legales o de compliance (GDPR, ISO, etc.) que debamos contemplar?
2. Tecnología y equipo
    * ¿Qué stack tecnológico prefiere el equipo (Java, .NET, Node.js, React…)?
    * ¿Disponemos de servicios de IA propios o usaremos terceros (OpenAI, Azure Cognitive Services…)?
3. Integraciones y datos legacy
    * ¿Debemos integrarnos con algún sistema HRIS existente (SAP, Workday, BambooHR…)?
    * ¿Existe ya una base de datos de candidatos a migrar?
4. Timeline y recursos
    * ¿Cuál es la fecha objetivo de lanzamiento del MVP?
    * ¿Con qué tamaño de equipo contamos para desarrollo, QA y operaciones?
5. Usuarios y métricas
    * ¿Cómo mediremos el éxito (KPI’s: time-to-hire, candidate NPS, adopción interna…)?
    * ¿Háblame del perfil y número estimado de usuarios concurrentes en el MVP?

Con estos Meta-prompts y preguntas iniciales, podrás alinear a tu equipo y a la IA sobre qué, cómo y por qué de cada fase, asegurando cobertura completa de todos los entregables. ¿Qué otros aspectos crees que deberíamos explorar antes de arrancar?