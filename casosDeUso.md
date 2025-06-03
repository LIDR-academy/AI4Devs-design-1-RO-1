## 🎭 Casos de Uso Principales

### 1️⃣ Caso de Uso: Publicación y Gestión de Ofertas Laborales

**Actor Principal:** Reclutador/HR Manager  
**Objetivo:** Crear y publicar ofertas de trabajo de manera eficiente en múltiples canales

#### Descripción Detallada:

**Precondiciones:**
- El usuario está autenticado en el sistema
- Tiene permisos para crear ofertas laborales

**Flujo Principal:**
1. El reclutador accede al módulo "Crear Nueva Oferta"
2. Completa la información básica: título, descripción, requisitos, salario, ubicación
3. Define el pipeline de selección (etapas personalizadas)
4. Asigna hiring managers y colaboradores
5. Configura las integraciones de publicación (LinkedIn, Indeed, web corporativa)
6. El sistema valida la información y sugiere mejoras con IA
7. Publica la oferta automáticamente en los canales seleccionados
8. Genera un dashboard de seguimiento en tiempo real

**Flujos Alternativos:**
- Si hay campos incompletos, el sistema sugiere completar información faltante
- Si la integración con un portal falla, se notifica al usuario y se reintenta automáticamente

**Postcondiciones:**
- La oferta está activa y visible en todos los canales configurados
- Se inicia el tracking de aplicaciones entrantes
- Los stakeholders reciben notificaciones de la nueva oferta

#### Diagrama de Caso de Uso:

```
@startuml
left to right direction

actor Reclutador as R
actor "Hiring Manager" as HM
actor "Sistema IA" as IA

rectangle "Gestión de Ofertas Laborales" {
  R --> (Crear Nueva Oferta)
  R --> (Editar Oferta)
  R --> (Publicar Oferta)
  R --> (Ver Métricas)
  
  HM --> (Asignar Responsables)
  HM --> (Revisar Oferta)
  
  IA --> (Validar Información)
  IA --> (Sugerir Mejoras)
  
  (Publicar Oferta) .> (Integración LinkedIn) : <<include>>
  (Publicar Oferta) .> (Integración Indeed) : <<include>>
  (Crear Nueva Oferta) .> (Configurar Pipeline) : <<include>>
}
@enduml
```


### 2️⃣ Caso de Uso: Gestión Integral de Candidatos

**Actor Principal:** Reclutador, Hiring Manager  
**Objetivo:** Gestionar candidatos desde la aplicación hasta la decisión final

#### Descripción Detallada:

**Precondiciones:**
- Existen ofertas activas en el sistema
- Los candidatos han aplicado por diversos canales

**Flujo Principal:**
1. El candidato aplica a través de múltiples fuentes (LinkedIn, email, referido, web)
2. El sistema ingesta automáticamente el CV y crea el perfil
3. La IA realiza un match semántico con las ofertas abiertas
4. El reclutador revisa los candidatos en el dashboard priorizado
5. Accede al perfil completo: CV, historial, notas, evaluaciones
6. Realiza acciones: avanzar etapa, rechazar, agendar entrevista, añadir comentarios
7. Colabora con el equipo mediante menciones y asignación de tareas
8. El sistema registra toda la actividad y actualiza métricas

**Flujos Alternativos:**
- Si el CV no se puede parsear automáticamente, se solicita intervención manual
- Si hay candidatos duplicados, el sistema sugiere fusión de perfiles
- Si un candidato no responde, se activan flujos de seguimiento automatizado

**Postcondiciones:**
- El candidato avanza por el pipeline o es rechazado con feedback
- Se mantiene un historial completo de interacciones
- Las métricas del proceso se actualizan en tiempo real

#### Diagrama de Caso de Uso:
```
@startuml
left to right direction

actor Candidato as C
actor Reclutador as R
actor "Hiring Manager" as HM
actor "Sistema IA" as IA

rectangle "Gestión de Candidatos" {
  C --> (Aplicar a Oferta)
  
  R --> (Revisar Aplicaciones)
  R --> (Gestionar Perfil Candidato)
  R --> (Avanzar Etapa)
  R --> (Rechazar Candidato)
  
  HM --> (Evaluar Candidato)
  HM --> (Colaborar con Equipo)
  
  IA --> (Match Semántico)
  IA --> (Priorizar Candidatos)
  
  (Aplicar a Oferta) .> (Ingesta Automática CV) : <<include>>
  (Revisar Aplicaciones) .> (Ver Dashboard) : <<include>>
  (Gestionar Perfil Candidato) .> (Añadir Comentarios) : <<include>>
  (Colaborar con Equipo) .> (Menciones @usuario) : <<include>>
}
@enduml
```

---

### 3️⃣ Caso de Uso: Coordinación y Evaluación de Entrevistas

**Actor Principal:** Reclutador, Entrevistador, Candidato  
**Objetivo:** Organizar, ejecutar y evaluar entrevistas de manera eficiente

#### Descripción Detallada:

**Precondiciones:**
- El candidato ha avanzado a la etapa de entrevista
- Los entrevistadores están definidos y disponibles
- Las integraciones de calendario están configuradas

**Flujo Principal:**
1. El reclutador selecciona candidatos listos para entrevista
2. Consulta disponibilidad automática en Google Calendar/Outlook de los entrevistadores
3. Propone slots de tiempo considerando zonas horarias automáticamente
4. Configura el tipo de entrevista (presencial, remota vía Zoom/Meet, híbrida)
5. Envía invitaciones automáticas a todos los participantes
6. El día de la entrevista, los entrevistadores acceden al perfil del candidato
7. Durante/después de la entrevista, completan la evaluación en la plataforma
8. La IA genera un resumen automático del feedback
9. El sistema actualiza el estado del candidato y notifica al equipo

**Flujos Alternativos:**
- Si hay conflictos de horario, el sistema sugiere alternativas automáticamente
- Si la integración de videollamada falla, se proporcionan links de backup
- Si un entrevistador no puede asistir, se re-programa automáticamente

**Postcondiciones:**
- La entrevista queda registrada con evaluaciones completas
- Se genera feedback consolidado para toma de decisiones
- El candidato recibe seguimiento automático sobre próximos pasos

#### Diagrama de Caso de Uso:

```
@startuml
left to right direction

actor Reclutador as R
actor Entrevistador as E
actor Candidato as C
actor "Sistema Calendario" as SC
actor "Sistema IA" as IA

rectangle "Coordinación de Entrevistas" {
  R --> (Programar Entrevista)
  R --> (Configurar Tipo Entrevista)
  
  E --> (Evaluar Candidato)
  E --> (Completar Feedback)
  
  C --> (Participar en Entrevista)
  C --> (Recibir Invitación)
  
  SC --> (Consultar Disponibilidad)
  SC --> (Enviar Invitaciones)
  
  IA --> (Generar Resumen)
  IA --> (Analizar Feedback)
  
  (Programar Entrevista) .> (Integración Google Calendar) : <<include>>
  (Configurar Tipo Entrevista) .> (Zoom/Meet Integration) : <<include>>
  (Evaluar Candidato) .> (Actualizar Estado) : <<include>>
}
@enduml
````