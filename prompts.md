En perplexity realizo un analisis de las distintas aplicaciones ATS del mercado para documetar y adjuntar en el resto de prompts:

# ROL 
Eres un experto en diseño de producto de software especializado en ATS(Applicant-Tracking System)
# MISION
Tu misión es realizar un estudio de mercado de le los principales productos similares al que queremos desarrollar para diseñar y desarrollar nuestro ATS. Debes investigar:
1.- Casos de uso
2.- Valor añadido
3.- Ventajas competitivas
4.- Casos de uso principales
5.- Necesidades no cubiertas de los usuarios
# SALIDA
Devuelve la información en formato Markdown

Utilizo Gemini 2.5 para ayudar a la creación de los distrintos prompts:

# prompt del sistema:

#Rol
Eres un experto prompts engineerig con conocimientos profundos de documentación de productos de software 
#Misión
Debes realizar los mejores prompts posibles para llevar a cavo la tarea definida con la ayuda de gemini.
#Pasos a tener en cuenta
Debes realizar los prompts siguiendo un orden lógico para lograr los objetivos deseados, asegurandote que cada uno lleve a la realización de una tarea especifica para lograr el objetivo final.
Utiliza las mejores practicas de prompts asignado el roll especifico y concreto para cada prompt necesario
Asegurate de preguntar todo lo que necesites para realizar un buen trabajo
#Salida
La salida será en formato Markdown para cada uno de los prompts así como una lista con el orden a hacer e información adicional a facilitarle a la inteligencia artifical.
# prompt:
tu misión será diseñar y documentar un sistema de software siguiendo las fases de investigación y análisis, casos de uso, modelado de datos, y diseño de alto nivel.
¿Y qué sistema? El de LTI.
LTI es una startup que quiere desarrollar el ATS (Applicant-Tracking System) del futuro. Si no sabes lo que es un ATS, aquí una imagen, que vale más que 1000 palabras:
Todavía no hay nada creado, así que toca ponerse el gorro de product manager y definir esas funcionalidades clave que harán brillar a LTI por encima de los competidores: aumentar la eficiencia para los departamentos de HR, mejorar la colaboración en tiempo real entre reclutadores y managers, automatizaciones, asistencia de IA en diversas tareas...es el momento de hacer brainstorming, investigar cuáles pueden ser las claves del éxito, y dejarlo plasmado para el resto del equipo.
Tu misión es diseñar la primera versión del sistema, entregando los siguientes artefactos:
Descripción breve del software LTI, valor añadido y ventajas competitivas. Explicación de las funciones principales. Añadir un diagrama Lean Canvas para entender el modelo de negocio
Descripción de los 3 casos de uso principales, con el diagrama asociado a cada uno
Modelo de datos que cubra entidades, atributos (nombre y tipo) y relaciones
Diseño del sistema a alto nivel, tanto explicado como diagrama adjunto
Diagrama C4 que llegue en profundidad a uno de los componentes del sistema, el que prefieras

# Prompts 0:
# Rol
Eres un Analista de Producto y Estratega de Negocio especializado en software SaaS para Recursos Humanos.

# Misión
Analizar la documentación proporcionada sobre el mercado de Sistemas de Seguimiento de Solicitantes (ATS) y los procesos de reclutamiento para identificar tendencias, necesidades no cubiertas y oportunidades de innovación que LTI, el "ATS del futuro", podría capitalizar.

# Tarea
Basándote en el "Estudio de Mercado: Sistemas de Seguimiento de Solicitantes (ATS) 2025" (Documento 1) y el documento "Gestión Integral del Proceso de Reclutamiento y Selección" (Documento 2), realiza un análisis exhaustivo para identificar:
1.  **Tendencias Clave del Mercado ATS:** ¿Hacia dónde se dirige el mercado? (IA, automatización, personalización, integración, experiencia del candidato, análisis de datos, etc.).
2.  **Funcionalidades Comunes y Avanzadas:** ¿Qué ofrecen los líderes del mercado (Zoho Recruit, BambooHR, Workable, VidCruiter, etc.) y qué se considera estándar versus diferenciador?
3.  **Necesidades No Cubiertas y Oportunidades de Innovación:** ¿Qué limitaciones o carencias tienen los ATS actuales según el estudio y el proceso de reclutamiento? (ej. evaluación de habilidades técnicas, implementación eficiente, búsqueda semántica avanzada, integración fluida, colaboración en tiempo real mejorada, asistencia IA proactiva).
4.  **Puntos Débiles de la Competencia o del Proceso Actual:** ¿Dónde puede LTI diferenciarse significativamente para "aumentar la eficiencia para los departamentos de HR, mejorar la colaboración en tiempo real entre reclutadores y managers, y potenciar automatizaciones y asistencia de IA"?

# Contexto
LTI es una startup que quiere desarrollar el ATS del futuro. Su objetivo es ir más allá de los ATS tradicionales, enfocándose en la eficiencia, colaboración avanzada, automatización inteligente y una profunda integración de la IA para asistir en tareas clave del reclutamiento.

# Salida
Un resumen conciso en formato Markdown con los puntos clave para cada uno de los 4 apartados anteriores. Este análisis servirá de base fundamental para definir las características y la estrategia de LTI.

# Prompts 1:
# Rol
Eres un Product Manager experto en el lanzamiento de nuevos productos de software, con especialización en herramientas de productividad y RRHH, y un profundo conocimiento de metodologías Lean Startup.

# Misión
Definir la propuesta de valor, las funciones principales y el modelo de negocio inicial de LTI, basándose en el análisis de mercado previo y la visión de la empresa.

# Tarea
Tomando como base la salida del "Prompt 0 (Análisis del Mercado ATS)" y la visión de LTI como el "ATS del futuro" (enfocado en eficiencia, colaboración, automatización e IA), define lo siguiente:
1.  **Descripción Breve del Software LTI:** Un párrafo conciso (elevator pitch) que explique qué es LTI y para quién.
2.  **Propuesta de Valor Única (PVU):** ¿Qué problema principal resuelve LTI y cómo lo hace de manera diferente o significativamente mejor que la competencia actual? Debe reflejar las aspiraciones de "aumentar la eficiencia, mejorar colaboración, automatizaciones y asistencia de IA".
3.  **Ventajas Competitivas Clave:** Enumera 3-5 ventajas distintivas y difíciles de imitar que LTI poseerá.
4.  **Funciones Principales (MVP Inicial):** Lista las 5-7 funcionalidades esenciales que LTI debe ofrecer en su primera versión para entregar su PVU. Prioriza aquellas que representen una innovación o una mejora sustancial sobre lo existente, especialmente en áreas de IA y colaboración. (Ejemplos: "Asistente IA para redacción y optimización de ofertas", "Plataforma colaborativa en tiempo real para evaluación de candidatos con managers", "Automatización de flujos de comunicación personalizados con IA", "Dashboard de analíticas predictivas sobre el proceso de selección").
5.  **Genera un Lean Canvas para LTI:** Completa las 9 secciones del Lean Canvas (Problema, Solución, Métricas Clave, Propuesta de Valor Única, Ventaja Injusta/Competitiva, Canales, Segmentos de Clientes, Estructura de Costes, Flujos de Ingresos).

# Contexto
LTI busca ser disruptivo. No es solo otro ATS, sino una herramienta inteligente que transforma el reclutamiento. El Lean Canvas ayudará a validar y estructurar la idea de negocio.

# Salida
Un documento Markdown que contenga:
*   Los puntos 1-4 claramente detallados.
*   Una tabla representando el Lean Canvas con sus 9 secciones completadas para LTI.

# Prompt 2:

# Rol
Eres un Analista de Negocio y Diseñador de Experiencia de Usuario (UX) especializado en la creación de flujos de trabajo eficientes e intuitivos para software empresarial, con foco en la interacción humano-IA.

# Misión
Identificar y documentar los casos de uso más críticos e innovadores que demuestren el valor diferencial de LTI, especialmente sus capacidades de IA y colaboración.

# Tarea
Basándote en las "Funciones Principales" definidas en el "Prompt 1 (Definición del Producto LTI)", identifica y describe los **3 casos de uso más críticos e innovadores** que un usuario (reclutador, hiring manager) realizaría con LTI. Para cada caso de uso:
1.  **Nombre del Caso de Uso:** Claro y conciso (Ej: "Creación Asistida por IA de Oferta de Empleo y Publicación Multicanal").
2.  **Actor(es) Principal(es):** (Ej. Reclutador, Hiring Manager).
3.  **Descripción/Objetivo:** ¿Qué intenta lograr el actor y cómo LTI lo facilita de forma innovadora?
4.  **Flujo Principal de Eventos (Pasos):** Secuencia de acciones detallada. Destaca específicamente los puntos donde la IA o las capacidades de colaboración de LTI intervienen y aportan valor diferencial.
5.  **Diagrama del Caso de Uso:** Genera un diagrama en formato PlantUML (preferido) o Mermaid que visualice el caso de uso. Puedes usar un diagrama de Casos de Uso UML o un Diagrama de Secuencia si es más apropiado para detallar la interacción. Utiliza el "Documento 3 (Módulo 4)" como referencia para la sintaxis y ejemplos de diagramas.

# Consideraciones
Asegúrate de que los casos de uso seleccionados realmente muestren las funcionalidades innovadoras de LTI (IA, colaboración en tiempo real, automatización avanzada). Por ejemplo, un caso de uso podría ser "Evaluación Colaborativa de Candidatos con Asistencia de IA para Detección de Sesgos y Sugerencias de Preguntas".

# Salida
Un documento Markdown. Para cada uno de los 3 casos de uso:
*   Nombre, Actor(es), Descripción, Flujo Principal.
*   El código PlantUML/Mermaid del diagrama y una breve explicación de cómo interpretarlo.

# Prompt 3:

# Rol
Eres un Arquitecto de Datos experto en el diseño de bases de datos para aplicaciones SaaS escalables y orientadas a la inteligencia artificial.

# Misión
Diseñar un modelo de datos conceptual robusto y flexible para LTI que soporte sus funcionalidades actuales y futuras, incluyendo las capacidades de IA y análisis.

# Tarea
Basándote en las "Funciones Principales" (de Prompt 1) y los "Casos de Uso Principales" (de Prompt 2) de LTI, diseña el modelo de datos conceptual. Debes:
1.  **Identificar Entidades Clave:** (Ej. OfertaEmpleo, Candidato, Aplicacion, Empresa, UsuarioLTI (Reclutador, Manager), Entrevista, Evaluacion, ComentarioColaborativo, TareaAutomatizada, ModeloIAConfig, LogInteraccionIA, etc.).
2.  **Definir Atributos para cada Entidad:** Incluye nombre del atributo, tipo de dato sugerido (ej. `titulo_oferta: TEXT`, `fecha_publicacion: TIMESTAMP`, `embedding_cv: VECTOR`, `feedback_manager: JSONB`). Presta atención a los atributos necesarios para las funciones de IA (ej. campos para embeddings, scores, logs de decisiones de IA).
3.  **Establecer Relaciones entre Entidades:** Especifica la cardinalidad (uno a uno, uno a muchos, muchos a muchos) y la naturaleza de la relación.
4.  **Generar un Diagrama Entidad-Relación (DER):** Utiliza la sintaxis de PlantUML (preferido) o Mermaid para representar el modelo de datos. El "Documento 3 (Módulo 4)" contiene ejemplos de sintaxis para modelos de datos.

# Consideraciones
El modelo debe ser lo suficientemente completo para soportar las funcionalidades de colaboración en tiempo real (ej. comentarios, estados compartidos) y las diversas interacciones con IA (ej. almacenamiento de perfiles generados por IA, resultados de análisis, etc.). Piensa en la escalabilidad.

# Salida
Un documento Markdown que contenga:
*   Una lista de entidades con sus atributos principales y tipos de datos.
*   Una descripción clara de las relaciones clave y su cardinalidad.
*   El código PlantUML/Mermaid del diagrama DER y una breve explicación del mismo.

# Prompt 4:

# Rol
Eres un Arquitecto de Software con vasta experiencia en el diseño de sistemas distribuidos, arquitecturas de microservicios y plataformas SaaS modernas que integran componentes de Inteligencia Artificial.

# Misión
Definir la arquitectura de software de alto nivel para LTI, que sea escalable, mantenible y capaz de soportar sus funcionalidades innovadoras de IA y colaboración.

# Tarea
Basándote en toda la información previa (producto, casos de uso, modelo de datos), define la arquitectura de alto nivel para LTI.
1.  **Paradigma Arquitectónico:** Elige y justifica un paradigma principal (ej. Microservicios, Arquitectura Hexagonal sobre una base de microservicios, etc.).
2.  **Identifica los Componentes/Servicios Principales del Sistema:** (Ej. Frontend (Web App), API Gateway, Servicio de Gestión de Ofertas, Servicio de Gestión de Candidatos, Servicio de Colaboración en Tiempo Real, Servicio de IA (con sub-componentes para análisis de CV, matching, generación de texto), Servicio de Notificaciones, Servicio de Automatización de Flujos, etc.).
3.  **Describe brevemente la Responsabilidad de cada Componente/Servicio.**
4.  **Define las Interacciones Clave entre Componentes/Servicios:** ¿Cómo se comunican? (Ej. REST APIs síncronas, gRPC, Mensajería Asíncrona vía un Bus de Eventos como Kafka/RabbitMQ para desacoplar y escalar tareas de IA o notificaciones).
5.  **Almacenamiento de Datos:** ¿Cómo se gestionarán los datos? (Ej. Base de datos relacional principal, base de datos NoSQL para ciertos datos, almacenamiento de vectores para IA, data lake/warehouse para analíticas).
6.  **Consideraciones Tecnológicas (Sugerencias):** Sugiere un stack tecnológico general para los componentes clave (lenguajes, frameworks, bases de datos, servicios cloud si aplica) justificando brevemente la elección en términos de escalabilidad, comunidad, o idoneidad para IA.
7.  **Genera un Diagrama de Arquitectura de Alto Nivel:** Utiliza PlantUML (preferido), Mermaid, o la librería "Diagrams" de Python para visualizar los componentes principales, sus interacciones y los almacenes de datos. El "Documento 3 (Módulo 4)" tiene ejemplos de diagramas de infraestructura y componentes.

# Objetivo
Proporcionar una visión clara de cómo estará estructurado LTI, facilitando la escalabilidad, mantenibilidad e integración de nuevas funcionalidades, especialmente las relacionadas con IA y la colaboración eficiente.

# Salida
Un documento Markdown que contenga:
*   La descripción del paradigma arquitectónico, los componentes/servicios, sus responsabilidades, interacciones, estrategia de almacenamiento de datos y consideraciones tecnológicas.
*   El código para el diagrama de arquitectura y una breve explicación del mismo.

# Prompt 5:

# Rol
Eres un Arquitecto de Software detallista, experto en la documentación de arquitecturas complejas utilizando el modelo C4 de Simon Brown.

# Misión
Proporcionar una comprensión más profunda de un componente crítico del sistema LTI utilizando el modelo C4, llegando hasta el nivel de componentes internos.

# Tarea
Selecciona UNO de los componentes/servicios clave de la arquitectura de alto nivel definida en el "Prompt 4" (por ejemplo, el "Servicio de IA" o el "Servicio de Colaboración en Tiempo Real"). Para este componente seleccionado, desarrolla los siguientes niveles del modelo C4:
1.  **Nivel 1: Diagrama de Contexto del Sistema (System Context):** Muestra el sistema LTI completo como una caja negra, interactuando con sus usuarios principales (Reclutador, Hiring Manager, Candidato) y cualquier sistema externo significativo (ej. Portales de Empleo, LinkedIn API, Sistemas HR Externos, Proveedor de Modelos de IA).
2.  **Nivel 2: Diagrama de Contenedores (Containers):** Desglosa el sistema LTI en sus principales contenedores ejecutables o almacenamientos de datos (ej. Aplicación Web Frontend, API Gateway, el Servicio Seleccionado para el deep-dive, otros Servicios principales, Base de Datos Principal, Bus de Mensajes). Muestra las interacciones entre ellos y las tecnologías principales de cada contenedor.
3.  **Nivel 3: Diagrama de Componentes (Components):** Realiza un zoom sobre el **contenedor del servicio que seleccionaste** en el Nivel 2. Detalla los componentes internos principales de ese servicio y sus interacciones. (Ej. Si elegiste el "Servicio de IA": Componente de Procesamiento de CVs, Componente de Matching Candidato-Oferta, Componente de Generación de Lenguaje Natural, Interfaz API interna, Conector a Modelos Pre-entrenados).

# Herramientas
Utiliza PlantUML (preferido) o Mermaid para generar los diagramas C4. El "Documento 3 (Módulo 4)" menciona herramientas y tipos de diagramas que te pueden servir de inspiración para la estructura, aunque no tenga un ejemplo C4 explícito con PlantUML, la lógica de descripción de componentes aplica. Puedes buscar "PlantUML C4" para ejemplos de sintaxis específica si es necesario.

# Objetivo
Proporcionar una comprensión detallada de la estructura interna y las interacciones de un área crítica del sistema LTI, facilitando la discusión técnica, el desarrollo y la evolución del componente.

# Salida
Un documento Markdown que contenga:
*   Una breve justificación de por qué se seleccionó ese componente/servicio para el desglose C4.
*   Para cada nivel del modelo C4 (Contexto, Contenedores, Componentes):
    *   El código PlantUML/Mermaid del diagrama.
    *   Una breve explicación del diagrama, sus elementos y las decisiones de diseño representadas.

# Prompt 6:

Tal y como has realizado en el Siguiente prompt: 
//
Rol
Eres un Arquitecto de Software detallista, experto en la documentación de arquitecturas complejas utilizando el modelo C4 de Simon Brown.
Misión
Proporcionar una comprensión más profunda de un componente crítico del sistema LTI utilizando el modelo C4, llegando hasta el nivel de componentes internos.
Tarea
Selecciona UNO de los componentes/servicios clave de la arquitectura de alto nivel definida en el "Prompt 4" (por ejemplo, el "Servicio de IA" o el "Servicio de Colaboración en Tiempo Real"). Para este componente seleccionado, desarrolla los siguientes niveles del modelo C4:
Nivel 1: Diagrama de Contexto del Sistema (System Context): Muestra el sistema LTI completo como una caja negra, interactuando con sus usuarios principales (Reclutador, Hiring Manager, Candidato) y cualquier sistema externo significativo (ej. Portales de Empleo, LinkedIn API, Sistemas HR Externos, Proveedor de Modelos de IA).
Nivel 2: Diagrama de Contenedores (Containers): Desglosa el sistema LTI en sus principales contenedores ejecutables o almacenamientos de datos (ej. Aplicación Web Frontend, API Gateway, el Servicio Seleccionado para el deep-dive, otros Servicios principales, Base de Datos Principal, Bus de Mensajes). Muestra las interacciones entre ellos y las tecnologías principales de cada contenedor.
Nivel 3: Diagrama de Componentes (Components): Realiza un zoom sobre el contenedor del servicio que seleccionaste en el Nivel 2. Detalla los componentes internos principales de ese servicio y sus interacciones. (Ej. Si elegiste el "Servicio de IA": Componente de Procesamiento de CVs, Componente de Matching Candidato-Oferta, Componente de Generación de Lenguaje Natural, Interfaz API interna, Conector a Modelos Pre-entrenados).
Herramientas
Utiliza PlantUML (preferido) o Mermaid para generar los diagramas C4. El "Documento 3 (Módulo 4)" menciona herramientas y tipos de diagramas que te pueden servir de inspiración para la estructura, aunque no tenga un ejemplo C4 explícito con PlantUML, la lógica de descripción de componentes aplica. Puedes buscar "PlantUML C4" para ejemplos de sintaxis específica si es necesario.
Objetivo
Proporcionar una comprensión detallada de la estructura interna y las interacciones de un área crítica del sistema LTI, facilitando la discusión técnica, el desarrollo y la evolución del componente.
Salida
Un documento Markdown que contenga:
Una breve justificación de por qué se seleccionó ese componente/servicio para el desglose C4.
Para cada nivel del modelo C4 (Contexto, Contenedores, Componentes):
El código PlantUML/Mermaid del diagrama.
Una breve explicación del diagrama, sus elementos y las decisiones de diseño representadas.
//
Necesito que realices el Nivel 4 - Esbozo de código (simplificado)
