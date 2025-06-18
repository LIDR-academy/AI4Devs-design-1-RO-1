# LTI - Applicant Tracking System del Futuro

**LTI** es un sistema ATS (Applicant Tracking System) diseñado para revolucionar el proceso de selección de talento en empresas modernas. A través de la automatización inteligente, la colaboración en tiempo real y la asistencia basada en IA, LTI mejora la eficiencia de los equipos de recursos humanos, desde la publicación de vacantes hasta la contratación final.

## 🚀 Valor añadido

* Automatización de tareas repetitivas: filtrado de CVs, programación de entrevistas, seguimiento de candidatos.
* Colaboración fluida: feedback compartido entre recruiters y hiring managers en tiempo real.
* Asistencia con IA: redacción de ofertas, análisis de perfiles, respuestas automáticas a candidatos.

## ⭐ Ventajas competitivas

* IA generativa integrada en el flujo de selección.
* Interfaz centrada en la experiencia del reclutador.
* Capacidad de integrarse fácilmente con otras plataformas (LinkedIn, Slack, Gmail, etc).

---

## Lean Canvas - LTI ATS

| Sección              | Contenido                                                                                             |
| -------------------- | ----------------------------------------------------------------------------------------------------- |
| Problema             | Procesos de selección lentos, poco colaborativos y sin automatización.                                |
| Solución             | ATS con automatización, colaboración en tiempo real y asistencia IA.                                  |
| Métricas clave       | Tiempo medio de contratación, tasa de conversión de candidatos, tasa de uso de funciones automáticas. |
| Propuesta de valor   | Reducción del tiempo de selección, mejor experiencia del candidato, decisiones más informadas.        |
| Ventaja diferencial  | Asistentes de IA integrados + colaboración en tiempo real.                                            |
| Canales              | RRSS, ferias de empleo, asociaciones de RRHH, LinkedIn, recomendaciones.                              |
| Segmento de clientes | Empresas medianas y grandes, startups en crecimiento, departamentos de RRHH.                          |
| Estructura de costos | Desarrollo, hosting, marketing, soporte técnico, licencias IA.                                        |
| Fuentes de ingresos  | Suscripción mensual por usuario, integración con sistemas externos, licencias premium.                |

---

## Casos de uso principales

### Caso de uso 1: Publicar una oferta

**Actor principal:** Reclutador
**Descripción:** El reclutador crea una nueva oferta desde un formulario y se publica automáticamente en portales de empleo conectados.

### Caso de uso 2: Filtrar candidatos automáticamente

**Actor principal:** Sistema (IA)
**Descripción:** El sistema aplica filtros automáticos a las hojas de vida basándose en los requerimientos definidos en la oferta.

### Caso de uso 3: Colaboración y feedback

**Actor principal:** Reclutador y Manager
**Descripción:** Ambos pueden dejar comentarios sobre los candidatos desde el panel, y decidir si continuar con ellos.

---

## Modelo de datos (entidades y relaciones)

### Usuario

* id: int
* nombre: string
* email: string
* rol: enum \[reclutador, manager]

### Oferta

* id: int
* titulo: string
* descripcion: text
* fecha\_publicacion: date
* usuario\_id: int (FK)

### Candidato

* id: int
* nombre: string
* email: string
* cv: text
* estado: enum \[nuevo, en proceso, rechazado, contratado]

### Aplicación

* id: int
* candidato\_id: int (FK)
* oferta\_id: int (FK)
* fecha\_aplicacion: date

---

## Diseño de sistema a alto nivel

### Arquitectura general

El sistema LTI se basa en una arquitectura modular compuesta por:

* **Frontend**: ReactJS
* **Backend**: Node.js con Express
* **Base de datos**: PostgreSQL
* **Servicios de IA**: integración con API de OpenAI
* **Integraciones externas**: LinkedIn, Slack, correo electrónico

Los módulos se comunican entre sí a través de APIs REST. El frontend consume los servicios backend de forma desacoplada, y la IA se usa como microservicio especializado.

---

## Diagrama C4: Motor de filtrado inteligente

### Contexto

El componente de "Motor de filtrado inteligente" se encarga de analizar los perfiles de los candidatos usando NLP para identificar la coincidencia con los requerimientos de las ofertas.

### Contenido del componente

**Entradas:**

* Criterios de la oferta (experiencia, habilidades, ubicación, etc.)
* Perfiles de los candidatos (CV, respuestas, calificaciones)

**Salidas:**

* Lista ordenada de candidatos sugeridos por relevancia

**Tecnologías involucradas:**

* OpenAI API / embeddings
* Motor de reglas internas (score heurístico)
* Cache de resultados recientes

Puedes crear el diagrama C4 usando herramientas como Structurizr, Diagrams.net o Excalidraw.

---

## Archivos entregables

```
📁 LTI-DR
├── LTI-DR.md          ← Documento principal con esta información
├── prompts.md         ← Archivo con los prompts usados para construir esta documentación
```
