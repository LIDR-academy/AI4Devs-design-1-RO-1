# 1. Resumen Ejecutivo de **LTI — Lean Talent Intelligence**

**Propósito**
LTI es una plataforma SaaS de *Recruiting Enablement* que centraliza todo el flujo de atracción, evaluación y contratación de talento, añadiendo IA generativa y automatizaciones “no-code” para multiplicar la productividad de HR y hiring managers.

| Valor añadido                                                                                                                                                                                                                                 | Ventajas competitivas                                                                                                                                                                                                                                                             |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| - Screening automático y ranking de candidatos.<br>- Colaboración en tiempo real (comentarios in-line, co-view de CVs).<br>- Programación de entrevistas 100 % automática.<br>- Copiloto de IA que redacta descripciones, correos y feedback. | - Reducción ≥ 40 % del *time-to-hire*.<br>- Experiencia unificada para Recruiters + Managers.<br>- Motor de IA propio entrenado con resultados de contratación.<br>- Arquitectura *event-driven* fácil de extender con integraciones ATS, Slack, Google Workspace, Microsoft 365. |

### Funcionalidades principales del MVP

1. **Job Booster** – Creación asistida por IA de descripciones y publicación multicanal.
2. **Smart Screening** – Parser de CV + ranking automático con explicaciones (IA explicable).
3. **Live Collab** – Pizarra de feedback en tiempo real entre recruiter y manager.
4. **Auto-Scheduling** – Integración calendario + preferencias del candidato → envía invitaciones.
5. **Insights & KPIs** – Dashboards de *funnel*, *time-to-hire*, *quality-of-hire*.

---

## Lean Canvas (versión 1)

| Problema (Top 3)                                                                                                                         | Segmentos de cliente                                                                                                                 | Propuesta de valor única                                                                          | Solución                                                                                   | Métricas clave                                                                         |
| ---------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------- |
| 1. Procesos de reclutamiento manuales y lentos.<br>2. Falta de visibilidad para managers.<br>3. Pérdida de talento por mala experiencia. | • Equipos de Talent Acquisition (50-5000 empleados).<br>• Hiring managers de empresas +200 empleados.<br>• Consultoras de selección. | “Contrata al mejor talento un 40 % más rápido con IA transparente y colaboración en tiempo real.” | 1. Smart Screening.<br>2. Live Collab.<br>3. Auto-Scheduling.                              | • Time-to-hire.<br>• % entrevistas agendadas sin intervención.<br>• NPS de candidatos. |
| Ventaja injusta                                                                                                                          | Canales                                                                                                                              | Estructura de costes                                                                              | Flujo de ingresos                                                                          |                                                                                        |
| Motor de IA entrenado con datos históricos de éxito y feedback explícito; red de socios ATS.                                             | • Content & SEO.<br>• Alianzas ATS/HRIS.<br>• Seminarios web.                                                                        | • Infra SaaS (cloud, IA).<br>• Equipo producto+IA.<br>• Ventas & CS.                              | • Suscripción por usuario/mes.<br>• Add-ons IA premium.<br>• Marketplace de integraciones. |                                                                                        |

---

# 2. Casos de uso principales

| # | Título                                 | Actores                            | Descripción breve                                                                                 | Objetivo                               |
| - | -------------------------------------- | ---------------------------------- | ------------------------------------------------------------------------------------------------- | -------------------------------------- |
| 1 | **Publicar posición con IA**           | Recruiter                          | Crea oferta → IA sugiere texto → Publica multi-portal                                             | Publicar rápido y coherente            |
| 2 | **Screening y ranking**                | Recruiter, IA Engine               | CVs entran → IA asigna score → Recruiter aprueba                                                  | Reducir tiempo filtrado                |
| 3 | **Feedback colaborativo & entrevista** | Manager, Recruiter, Calendario API | Manager revisa candidatos, deja feedback en tiempo real; LTI propone horario y envía invitaciones | Colaboración + programación automática |

### Diagramas de caso de uso (resumen textual)

```
(1) Publicar posición
Recruiter --> (Crear Oferta) --> [IA Description Helper]
Recruiter --> (Publicar) --> [Job Boards / ATS]

(2) Smart Screening
Recruiter --> (Revisar Lista) <-- [IA Scoring Engine] <-- (Procesar CV)
Recruiter --> (Mover a Entrevista)

(3) Colaboración & Entrevista
Manager --> (Dar Feedback) --> [Realtime Collab Hub] <-- Recruiter
[Realtime Collab Hub] --> (Generar Disponibilidad) --> Calendar API
Calendar API --> (Invitación) --> Candidate
```

---

# 3. Modelo de Datos (v0.1)

| Entidad                 | Atributos (nombre\:tipo)                                                                                                                   | Relaciones claves         |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------- |
| **User**                | id\:UUID, name\:String, email\:String, role\:Enum(`RECRUITER`,`MANAGER`,`ADMIN`), createdAt\:Date                                          | 1-\* Job, Feedback        |
| **Job**                 | id\:UUID, title\:String, description\:Text, status\:Enum(`OPEN`,`CLOSED`), ownerId\:UUID(FK User), createdAt\:Date                         | 1-\* Application          |
| **Candidate**           | id\:UUID, firstName\:String, lastName\:String, email\:String, resumeUrl\:String, createdAt\:Date                                           | 1-\* Application          |
| **Application**         | id\:UUID, jobId\:UUID, candidateId\:UUID, stage\:Enum(`SCREENING`,`INTERVIEW`,`OFFER`,`HIRED`,`REJECTED`), aiScore\:Float, createdAt\:Date | 1-\* Interview            |
| **Interview**           | id\:UUID, applicationId\:UUID, start\:DateTime, end\:DateTime, mode\:Enum(`ONLINE`,`ONSITE`), meetLink\:String                             | 1-\* Feedback             |
| **Feedback**            | id\:UUID, interviewId\:UUID, userId\:UUID, rating\:Int, comments\:Text, createdAt\:Date                                                    | \*                        |
| **Event** (audit / bus) | id\:UUID, type\:String, payload\:JSONB, timestamp\:DateTime                                                                                | Event-driven integrations |

**Relaciones destacadas**

* *User* (1) —— (N) *Job*
* *Job* (1) —— (N) *Application* ——— (N) *Candidate* (1)
* *Application* (1) —— (N) *Interview* —— (N) *Feedback* (1)

---

# 4. Diseño de Sistema (alto nivel)

### Componentes clave

1. **Frontend Web (React + Next.js)**

   * SPA con SSR para SEO.
   * WebSockets para Live Collab.
2. **API Gateway (GraphQL)**

   * Orquesta llamadas a microservicios.
   * Autenticación (JWT / OAuth2).
3. **User Service (NestJS + PostgreSQL)**
4. **Recruiting Service (NestJS + PostgreSQL)** – Jobs, Applications, Interviews.
5. **AI Service (Python FastAPI)** – Scoring, copilot (LLM), embeddings.
6. **Collaboration Hub (Node.js + Socket.io + Redis)**
7. **Scheduler Service** – Integración calendarios (Google / MS).
8. **Event Bus (RabbitMQ)** – Comunicación asíncrona.
9. **Notification Service** – Email, Slack, SMS.
10. **Search Service (Elasticsearch)** – Búsqueda avanzada de candidatos / jobs.
11. **File Storage (S3 compatible)** – CVs, adjuntos.
12. **Observability Stack (Grafana, Loki, Tempo).**

### Flujo típico

Frontend → GraphQL → Recruiting Service → Event `APPLICATION_CREATED` → AI Service calcula *aiScore* → Event Bus emite → Notification Service avisa al recruiter.

---

# 5. Diagrama C4 (profundizando en *AI Service*)

### Nivel 1 – Contexto

```
[Recruiter] --usa--> (LTI Platform) --depende--> {AI Service}
[Manager] ---------------------------------------^
```

### Nivel 2 – Contenedores

```
{AI Service}
  |-- CandidateRanker  (Python, scikit-learn/LLM)
  |-- JobDescriptionCopilot (LLM, prompt templates)
  |-- FeedbackSentiment (NLP)
  |-- REST / gRPC API
  |-- Vector DB (pgvector)
```

### Nivel 3 – Componentes dentro de **CandidateRanker**

| Componente               | Responsabilidad                          | Tecnología                   |
| ------------------------ | ---------------------------------------- | ---------------------------- |
| **Feature Extractor**    | Parseo de CV, embeddings, normalización. | spaCy, docx2txt              |
| **Model Ensembler**      | Random Forest + LLM scorer, ponderación. | scikit-learn + OpenAI GPT-4o |
| **Explainability Layer** | SHAP/LIME para justificaciones.          | shap                         |
| **Caching**              | Memoria de resultados frecuentes.        | Redis                        |

### Nivel 4 – Esbozo de código (simplificado)

```python
def rank(candidate, job_req):
    feats = extractor.transform(candidate, job_req)
    score_ml = rf_model.predict_proba([feats])[0,1]
    prompt = f"Evalúa el fit del candidato:\nCV: {candidate.text}\nJob:{job_req}"
    score_llm = llm.score(prompt)
    return 0.6*score_ml + 0.4*score_llm
```

---

## Conclusión

Con este set de artefactos—Lean Canvas, casos de uso, modelo de datos, diseño de arquitectura y C4—el equipo dispone de una visión coherente y accionable para construir el MVP de **LTI** y validar rápidamente su propuesta de valor frente al mercado.
