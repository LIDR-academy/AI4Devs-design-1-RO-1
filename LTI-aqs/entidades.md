# ✅ Entidades principales y atributos
## 1. User
Representa a los usuarios del sistema: reclutadores, managers, administradores.

|Atributo  | Tipo                              |
|----------|-----------------------------------|
|id        | UUID                              |
|name      | string                            |
|email	   | string                            |
|role	   | enum (recruiter, manager, admin)  |
|createdAt | datetime                          |

## 2. Job
Vacante publicada o en borrador.

|Atributo   | Tipo                              |
|-----------|-----------------------------------|
|id	        |   UUID                            |
|title      |	string                          |
|description|	text                            |
|department	|   string                          |
|location   |	string                          |
|status     |	enum (draft, open, closed)      |
|createdBy  |	FK → User                       |
|createdAt  |	datetime                        |

## 3. Application
Postulación de un candidato a un trabajo.

|Atributo   | Tipo                                                      |
|-----------|-----------------------------------------------------------|
|id	        |   UUID                                                    |
|jobId      |	FK → Job                                                |
|candidateId|	FK → Candidate                                          |
|status	    |   enum (new, reviewed, rejected, interviewed, hired)      |
|source	    |   string (e.g., "LinkedIn", "Referral")                   |
|createdAt  |	datetime                                                |

## 4. Candidate
Persona postulante al sistema.

|Atributo   | Tipo                                                      |
|-----------|-----------------------------------------------------------|
|id	        |   UUID                                                    |
|fullName   |	string                                                  |
|email	    |   string                                                  |
|phone	    |   string                                                  |
|resumeUrl	|   string                                                  |
|createdAt	|   datetime                                                |

## 5. Feedback
Opiniones y evaluaciones de los usuarios sobre postulaciones.

|Atributo       | Tipo                                                  |
|---------------|-------------------------------------------------------|
|id	            |   UUID                                                |
|applicationId  |	FK → Application                                    |
|reviewerId     |	FK → User                                           |
|rating         |	integer (1-5)                                       |
|comments       |	text                                                |
|createdAt      |	datetime                                            |

## 6. IAAnalysis
Resultados de la IA sobre un CV o perfil.

|Atributo       | Tipo                                                  |
|---------------|-------------------------------------------------------|
|applicationId  |	FK → Application                                    |
|summary        |	text                                                |
|strengths      |	json/text                                           |
|weaknesses	    |   json/text                                           |
|fitScore	    |   float (0-1)                                         |
|generatedAt	|   datetime                                            |

## 7. JobApproval
Registro de aprobación de una vacante.

|Atributo   | Tipo                                                      |
|-----------|-----------------------------------------------------------|
|id	        |   UUID                                                    |
|jobId      |	FK → Job                                                |
|approverId |	FK → User                                               |
|approved   |	boolean                                                 |
|reviewedAt |	datetime                                                |
|comments   |	text                                                    |

## 8. Tag
Etiqueta colaborativa sobre una postulación.

|Atributo   | Tipo                                                      |
|-----------|-----------------------------------------------------------|
|id	        |   UUID                                                    |
|name       |	string                                                  |

## 9. ApplicationTag
Relación N:M entre Tags y Applications.

|Atributo       | Tipo                                                  |
|---------------|-------------------------------------------------------|
|applicationId  |	FK → Application                                    |
|tagId	        |   FK → Tag                                            |

# ✅ Relaciones
* User → Job: 1:N (un usuario puede crear muchos trabajos)
* Job → Application: 1:N
* Candidate → Application: 1:N
* Application → Feedback: 1:N (múltiples evaluaciones por candidato)
* Application → IAAnalysis: 1:1
* Job → JobApproval: 1:N
* Application ↔ Tag: N:M (por medio de ApplicationTag)

# 🔁 Futuro (entidades no-MVP)
Estas entidades podrían añadirse más adelante:
* Interview: estructura de entrevistas y agenda.
* HiringPipeline: etapas definidas por trabajo.
* AutomationRule: sistema de automatización (si esto/entonces aquello).
* Notification: sistema de alertas internas.