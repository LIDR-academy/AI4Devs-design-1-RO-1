# Prompt inicial

Eres un arquitecto de software experto, quiero que me ayudes a diseñar y documentar un sistema de software siguiendo las fases de investigación y análisis, casos de uso, modelado de datos y diseño de alto nivel.

El proyecto sobre el que vamos a trabajar es sobre un Applicant Tracking System, no hay nada creado aún, y queremos que nuestro sistema tenga unas funcionalidades clave que harán brillar a LTI (nuestra startup) por encima de los competidores.

Puntos importantes para diferenciar nuestro sistema:
- Aumentar la eficiencia para los departamentos de HR
- Mejorar la colaboración en tiempo real entre reclutadores y managers
- Automatizaciones
- Asistencia de IA en diversas tareas

Quiero que me ayudes a diseñar la primera versión del sistema siguiendo estos pasos:
1. Investigación y análisis de requisitos: descripción breve del software de LTI, valor añadido y ventajas competitivas, así como explicación de las principales funciones a añadir, y un diagrama Lean Canvas para entender el modelo de negocio
2. Definición de casos de uso: 3 casos de uso principales con el diagrama asociado a cada uno
3. Modelado de datos: que cubra entidades, atributos (nombre y tipo) y relaciones
4. Diseño del sistema y arquitectura de alto nivel: explicado y con diagrama adjunto
5. Documentación: Diagrama C4 que llegue a profundidad a uno de los componentes del sistema

Todo esto tiene que quedar en un único documento markdown (.md).

Hazme de 4 a 6 preguntas para aclarar algunas cosas si es necesario.


# Preguntas Claude 4 Sonnet

## Preguntas hechas por el modelo

Perfecto, me ayudarás a diseñar un Applicant Tracking System innovador para LTI. Antes de comenzar con el análisis y diseño completo, necesito aclarar algunos aspectos clave para asegurar que el sistema cumpla exactamente con sus necesidades y visión:

Preguntas de Clarificación
1. Escala y Audiencia Target:
¿Están enfocados en empresas pequeñas/medianas (50-500 empleados) o también grandes corporaciones (500+ empleados)? ¿Hay algún sector específico (tech, healthcare, retail) o será generalista?
2. Funcionalidades de IA Específicas:
Cuando mencionas "asistencia de IA", ¿te refieres a funciones como screening automático de CVs, generación de preguntas de entrevista, análisis de sentimientos en entrevistas, matching candidato-puesto, o tienes otras capacidades específicas en mente?
3. Colaboración en Tiempo Real:
¿Qué tipo de colaboración específica visualizas? Por ejemplo: comentarios en tiempo real sobre candidatos, chat integrado, votación colaborativa, paneles compartidos, o algo más específico?
4. Integraciones Clave:
¿Hay sistemas externos críticos con los que debe integrarse? (LinkedIn, Indeed, sistemas de HR existentes como Workday/BambooHR, herramientas de videoconferencia, etc.)
5. Automatizaciones Prioritarias:
¿Cuáles son las 2-3 automatizaciones más importantes que deben estar en la v1? (envío de emails, scheduling de entrevistas, generación de reportes, actualización de estados, etc.)
6. Modelo de Deployment:
¿Prefieren SaaS multi-tenant, on-premise, o ambas opciones? ¿Hay consideraciones específicas de compliance (GDPR, CCPA) por región geográfica?

Con estas respuestas podré crear un diseño mucho más preciso y alineado con la visión de LTI.


## Respuestas dadas al modelo

1. Creo que estaremos enfocados en empresas pequeñas y medianas
2. 
- Anuncio de empleo y publicidad en 1 sólo click
- Sistema de rastreo de talentos y análisis de CV
- Tecnología patentada de puntuación y clasificación de candidatos
- Programación de entrevistas automatizada y gestionada por el candidato
- Comunicaciones automatizadas tanto con el candidato como con el equipo
- Entrevistas de selección automatizadas basadas en vídeo y potenciadas con PNL y puntuación
- Incorporación automatizada de las contrataciones
3. Las integraciones que sean la publicación automática de ofertas en LinkedIn y en Indeed, y que haya un scraper en LinkedIn para crear una BD de datos propia
4. No tengo idea
5. No hay que considerar ahorita el cumplimiento normativo
6. No tengo en mente competidores directos
