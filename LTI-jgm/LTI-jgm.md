# Sistema ATS LTI - Análisis y Diseño Completo

## 1. Descripción del Sistema y Modelo de Negocio

### Descripción del Software LTI

**LTI ATS** es una plataforma de gestión de talento de nueva generación que revoluciona el proceso de reclutamiento mediante la integración de inteligencia artificial, colaboración en tiempo real y automatizaciones inteligentes. El sistema está diseñado para eliminar las fricciones tradicionales entre departamentos de HR, managers y candidatos, creando un ecosistema colaborativo donde cada stakeholder puede contribuir de manera eficiente al proceso de selección.

La plataforma combina capacidades avanzadas de análisis predictivo para identificar los mejores candidatos, herramientas de comunicación integradas que facilitan la toma de decisiones colaborativa, y flujos de trabajo automatizados que reducen significativamente el tiempo de contratación. LTI no solo gestiona aplicaciones, sino que actúa como un asistente inteligente que aprende de cada proceso para optimizar continuamente los resultados de reclutamiento.

El sistema se posiciona como la solución integral que transforma el reclutamiento de una tarea administrativa reactiva a una función estratégica proactiva, permitiendo a las organizaciones atraer, evaluar y contratar el mejor talento de manera más rápida y precisa que nunca.

### Valor Añadido y Ventajas Competitivas

**Diferenciadores Clave:**

- **IA Conversacional Integrada**: Asistente de IA que puede pre-evaluar candidatos, generar preguntas de entrevista personalizadas y proporcionar insights sobre compatibilidad cultural
- **Colaboración en Tiempo Real**: Dashboard compartido donde HR y managers pueden comentar, evaluar y tomar decisiones simultáneamente
- **Automatización Predictiva**: Algoritmos que aprenden de decisiones pasadas para priorizar automáticamente candidatos y predecir probabilidades de éxito
- **Experiencia del Candidato Gamificada**: Portal interactivo que mantiene a los candidatos comprometidos durante todo el proceso
- **Integración Universal**: Conectores nativos con +50 plataformas (LinkedIn, Indeed, GitHub, etc.)
- **Analytics Avanzados**: Métricas predictivas sobre tiempo de contratación, calidad de hire y ROI por canal de reclutamiento

### Funciones Principales

1. **Gestión Inteligente de Candidatos**: Procesamiento automático de CVs con extracción de datos y scoring de compatibilidad
2. **Colaboración Multi-stakeholder**: Espacios de trabajo compartidos para equipos de reclutamiento
3. **Automatización de Workflows**: Secuencias personalizables de comunicación y seguimiento
4. **Portal del Candidato**: Experiencia self-service para aplicaciones y seguimiento de estatus
5. **Analytics e Insights**: Dashboards en tiempo real con métricas operativas y estratégicas
6. **Gestión de Entrevistas**: Scheduling inteligente y herramientas de evaluación estructurada

### Diagrama Lean Canvas

graph TB
    subgraph "LEAN CANVAS - LTI ATS"
        subgraph "1. PROBLEMA"
            P1["• Procesos de reclutamiento lentos (promedio 45 días)"]
            P2["• Falta de colaboración entre HR y managers"]
            P3["• 73% candidatos reportan experiencia deficiente"]
            P4["• Decisiones subjetivas sin datos predictivos"]
            P5["• ATS tradicionales no escalan con crecimiento"]
        end
        
        subgraph "2. SOLUCIÓN"
            S1["• IA Conversacional para pre-screening automático"]
            S2["• Dashboard colaborativo en tiempo real"]
            S3["• Automatización predictiva de workflows"]
            S4["• Portal del candidato gamificado y transparente"]
            S5["• Analytics avanzados con insights accionables"]
        end
        
        subgraph "3. MÉTRICAS CLAVE"
            M1["• ARR (Annual Recurring Revenue)"]
            M2["• Monthly Churn Rate < 3%"]
            M3["• Net Promoter Score > 60"]
            M4["• Time to Value < 21 días"]
            M5["• Cost per Acquisition vs LTV 1:5"]
        end
        
        subgraph "4. PROPUESTA DE VALOR ÚNICA"
            UV["El único ATS que reduce tiempo de contratación 60% mediante IA conversacional y colaboración en tiempo real, garantizando mejor calidad de hire"]
        end
        
        subgraph "5. VENTAJA ESPECIAL"
            A1["• Algoritmos propietarios de matching con ML"]
            A2["• Network effects: más datos = mejor precisión"]
            A3["• Patent-pending en IA conversacional para HR"]
            A4["• Partnerships exclusivos con LinkedIn y GitHub"]
        end
        
        subgraph "6. CANALES"
            CH1["• Inside Sales (B2B directo)"]
            CH2["• Content Marketing & SEO"]
            CH3["• Partners de implementación"]
            CH4["• HR Tech conferences & webinars"]
            CH5["• Freemium model para startups"]
        end
        
        subgraph "7. SEGMENTO DE CLIENTES"
            C1["• Scale-ups (50-500 empleados) - Early Adopters"]
            C2["• Empresas medianas (500-2000 empleados)"]
            C3["• Enterprise (2000+ empleados) - Premium"]
            C4["• Agencias de reclutamiento especializadas"]
        end
        
        subgraph "8. ESTRUCTURA DE COSTOS"
            CO1["• I+D y Desarrollo de Producto (45%)"]
            CO2["• Sales & Marketing (30%)"]
            CO3["• Infraestructura Cloud & AI (15%)"]
            CO4["• Operaciones y Soporte (10%)"]
        end
        
        subgraph "9. FLUJO DE INGRESOS"
            R1["• SaaS Tiered: €35-€120/usuario/mes"]
            R2["• Setup & Onboarding: €5K-€50K"]
            R3["• AI Premium Features: +€25/usuario/mes"]
            R4["• Professional Services: €150/hora"]
            R5["• Marketplace de integraciones: 15% rev share"]
        end
    end

## 2. Casos de Uso

### Caso de Uso 1: Gestión Completa del Proceso de Reclutamiento

**Descripción Detallada:**
Este caso de uso abarca todo el ciclo de vida del reclutamiento, desde la publicación de una vacante hasta la contratación final. El sistema automatiza tareas repetitivas, facilita la colaboración entre stakeholders y proporciona insights para optimizar el proceso.

**Actores:**
- Reclutador (Principal)
- Hiring Manager (Secundario)
- Candidato (Secundario)
- Sistema de IA (Secundario)

**Flujo Principal:**
1. Reclutador crea nueva vacante con requisitos y criterios
2. Sistema sugiere canales de publicación óptimos basado en datos históricos
3. IA procesa aplicaciones entrantes y genera scoring automático
4. Reclutador y Hiring Manager revisan candidatos pre-filtrados
5. Sistema programa entrevistas automáticamente
6. Evaluaciones se centralizan en dashboard colaborativo
7. IA proporciona recomendaciones finales basadas en todos los datos
8. Decisión final se comunica automáticamente a todos los candidatos

**Precondiciones:**
- Usuario autenticado con permisos de reclutador
- Plantillas de vacantes configuradas
- Integraciones con job boards activas

**Postcondiciones:**
- Vacante completada o archivada
- Datos del proceso almacenados para learning del sistema
- Métricas actualizadas en dashboards
- Candidatos no seleccionados quedan en talent pool

#### Diagrama

graph TB
    subgraph "Caso de Uso 1: Gestión Completa del Proceso de Reclutamiento"
        UC1[Crear Nueva Vacante]
        UC2[Publicar en Job Boards]
        UC3[Procesar Aplicaciones]
        UC4[Realizar Pre-screening con IA]
        UC5[Programar Entrevistas]
        UC6[Gestionar Pipeline de Candidatos]
        UC7[Tomar Decisión Final]
        UC8[Comunicar Resultados]
        UC9[Generar Reportes del Proceso]
    end
    
    Reclutador --> UC1
    Reclutador --> UC2
    Reclutador --> UC3
    Reclutador --> UC5
    Reclutador --> UC6
    Reclutador --> UC8
    Reclutador --> UC9
    
    HiringManager[Hiring Manager] --> UC6
    HiringManager --> UC7
    
    Candidato --> UC3
    Candidato --> UC5
    
    SistemaIA[Sistema IA] --> UC4
    SistemaIA --> UC6
    
    UC1 -.includes.-> UC2
    UC3 -.includes.-> UC4
    UC6 -.includes.-> UC5
    UC7 -.includes.-> UC8
    UC8 -.includes.-> UC9
    
    UC4 -.extends.-> UC3
    UC9 -.extends.-> UC7

### Caso de Uso 2: Evaluación Colaborativa de Candidatos

**Descripción Detallada:**
Facilita la evaluación conjunta de candidatos entre múltiples stakeholders, proporcionando herramientas de comunicación en tiempo real, sistemas de scoring estructurado y consolidación automática de feedback.

**Actores:**
- Hiring Manager (Principal)
- Reclutador (Principal)
- Miembros del equipo (Secundario)
- Candidato (Secundario)

**Flujo Principal:**
1. Candidato completa evaluaciones técnicas y culturales
2. Stakeholders acceden a perfil completo del candidato
3. Cada evaluador registra feedback estructurado
4. Sistema facilita discusiones en tiempo real sobre candidatos
5. IA identifica consensos y discrepancias
6. Dashboard consolida todas las evaluaciones
7. Recomendación final se genera automáticamente
8. Decisión se documenta con razonamiento completo

**Precondiciones:**
- Candidato ha completado aplicación inicial
- Evaluadores asignados al proceso
- Criterios de evaluación definidos

**Postcondiciones:**
- Decisión documentada y comunicada
- Feedback almacenado para referencias futuras
- Métricas de colaboración actualizadas

#### Diagrama

graph TB
    subgraph "Caso de Uso 2: Evaluación Colaborativa de Candidatos"
        UC1[Acceder a Perfil de Candidato]
        UC2[Realizar Evaluación Técnica]
        UC3[Evaluar Fit Cultural]
        UC4[Registrar Feedback Estructurado]
        UC5[Participar en Discusión Colaborativa]
        UC6[Consolidar Evaluaciones]
        UC7[Generar Recomendación Final]
        UC8[Documentar Decisión]
    end
    
    HiringManager[Hiring Manager] --> UC1
    HiringManager --> UC3
    HiringManager --> UC4
    HiringManager --> UC5
    HiringManager --> UC7
    HiringManager --> UC8
    
    Reclutador --> UC1
    Reclutador --> UC4
    Reclutador --> UC5
    Reclutador --> UC6
    Reclutador --> UC8
    
    MiembroEquipo[Miembro del Equipo] --> UC2
    MiembroEquipo --> UC4
    MiembroEquipo --> UC5
    
    Candidato --> UC2
    Candidato --> UC3
    
    SistemaIA[Sistema IA] --> UC6
    SistemaIA --> UC7
    
    UC1 -.includes.-> UC2
    UC1 -.includes.-> UC3
    UC2 -.includes.-> UC4
    UC3 -.includes.-> UC4
    UC4 -.includes.-> UC5
    UC5 -.includes.-> UC6
    UC6 -.includes.-> UC7
    UC7 -.includes.-> UC8
    
    UC5 -.extends.-> UC4
    UC6 -.extends.-> UC5

### Caso de Uso 3: Análisis Predictivo y Optimización

**Descripción Detallada:**
Utiliza datos históricos y machine learning para proporcionar insights predictivos sobre el éxito de contrataciones, optimizar estrategias de sourcing y predecir necesidades futuras de talento.

**Actores:**
- HR Director (Principal)
- Reclutador (Secundario)
- Sistema de Analytics (Principal)

**Flujo Principal:**
1. Sistema analiza patrones históricos de contratación
2. IA identifica factores de éxito y fracaso
3. Predicciones se generan para candidatos actuales
4. Recomendaciones de optimización del proceso se proporcionan
5. Dashboards ejecutivos se actualizan con insights
6. Alertas proactivas sobre tendencias críticas
7. Estrategias de sourcing se ajustan automáticamente
8. ROI de canales de reclutamiento se calcula y reporta

**Precondiciones:**
- Datos históricos suficientes (mínimo 6 meses)
- Integraciones con sistemas HRIS configuradas
- KPIs definidos y medibles

**Postcondiciones:**
- Modelos predictivos actualizados
- Recomendaciones estratégicas disponibles
- Dashboards ejecutivos actualizados

#### Diagrama

graph TB
    subgraph "Caso de Uso 3: Análisis Predictivo y Optimización"
        UC1[Analizar Datos Históricos]
        UC2[Generar Modelos Predictivos]
        UC3[Predecir Éxito de Candidatos]
        UC4[Optimizar Estrategias de Sourcing]
        UC5[Calcular ROI por Canal]
        UC6[Generar Dashboards Ejecutivos]
        UC7[Crear Alertas Proactivas]
        UC8[Recomendar Mejoras de Proceso]
    end
    
    HRDirector[HR Director] --> UC1
    HRDirector --> UC4
    HRDirector --> UC5
    HRDirector --> UC6
    HRDirector --> UC8
    
    Reclutador --> UC3
    Reclutador --> UC5
    Reclutador --> UC7
    
    SistemaAnalytics[Sistema Analytics] --> UC1
    SistemaAnalytics --> UC2
    SistemaAnalytics --> UC3
    SistemaAnalytics --> UC4
    SistemaAnalytics --> UC5
    SistemaAnalytics --> UC6
    SistemaAnalytics --> UC7
    SistemaAnalytics --> UC8
    
    Administrador --> UC2
    
    UC1 -.includes.-> UC2
    UC2 -.includes.-> UC3
    UC1 -.includes.-> UC4
    UC1 -.includes.-> UC5
    UC3 -.includes.-> UC6
    UC4 -.includes.-> UC6
    UC5 -.includes.-> UC6
    UC6 -.includes.-> UC7
    UC1 -.includes.-> UC8
    
    UC7 -.extends.-> UC6
    UC8 -.extends.-> UC6

## 3. Modelo de Datos

### Entidades Principales

**1. Usuario**
- id: UUID (Primary Key)
- email: VARCHAR(255) NOT NULL UNIQUE
- password_hash: VARCHAR(255) NOT NULL
- first_name: VARCHAR(100) NOT NULL
- last_name: VARCHAR(100) NOT NULL
- role: ENUM('admin', 'recruiter', 'hiring_manager', 'team_member')
- company_id: UUID (Foreign Key)
- is_active: BOOLEAN DEFAULT TRUE
- created_at: TIMESTAMP
- updated_at: TIMESTAMP

**2. Empresa**
- id: UUID (Primary Key)
- name: VARCHAR(255) NOT NULL
- domain: VARCHAR(100) UNIQUE
- industry: VARCHAR(100)
- size: ENUM('startup', 'small', 'medium', 'large', 'enterprise')
- subscription_plan: ENUM('basic', 'professional', 'enterprise')
- billing_email: VARCHAR(255)
- created_at: TIMESTAMP
- updated_at: TIMESTAMP

**3. Vacante**
- id: UUID (Primary Key)
- title: VARCHAR(255) NOT NULL
- description: TEXT
- requirements: JSON
- salary_range_min: DECIMAL(10,2)
- salary_range_max: DECIMAL(10,2)
- location: VARCHAR(255)
- remote_option: BOOLEAN DEFAULT FALSE
- employment_type: ENUM('full_time', 'part_time', 'contract', 'internship')
- experience_level: ENUM('entry', 'mid', 'senior', 'executive')
- status: ENUM('draft', 'active', 'paused', 'closed', 'filled')
- priority: ENUM('low', 'medium', 'high', 'urgent')
- created_by: UUID (Foreign Key)
- assigned_recruiters: JSON
- hiring_managers: JSON
- created_at: TIMESTAMP
- updated_at: TIMESTAMP
- deadline: TIMESTAMP

**4. Candidato**
- id: UUID (Primary Key)
- email: VARCHAR(255) NOT NULL
- first_name: VARCHAR(100) NOT NULL
- last_name: VARCHAR(100) NOT NULL
- phone: VARCHAR(20)
- linkedin_url: VARCHAR(500)
- github_url: VARCHAR(500)
- portfolio_url: VARCHAR(500)
- location: VARCHAR(255)
- current_position: VARCHAR(255)
- current_company: VARCHAR(255)
- experience_years: INTEGER
- skills: JSON
- education: JSON
- resume_url: VARCHAR(500)
- source: VARCHAR(100)
- ai_score: DECIMAL(5,2)
- created_at: TIMESTAMP
- updated_at: TIMESTAMP

**5. Aplicación**
- id: UUID (Primary Key)
- job_id: UUID (Foreign Key)
- candidate_id: UUID (Foreign Key)
- status: ENUM('new', 'screening', 'interview', 'assessment', 'offer', 'hired', 'rejected', 'withdrawn')
- applied_at: TIMESTAMP
- current_stage: VARCHAR(100)
- ai_compatibility_score: DECIMAL(5,2)
- recruiter_notes: TEXT
- rejection_reason: TEXT
- offer_details: JSON
- created_at: TIMESTAMP
- updated_at: TIMESTAMP

**6. Evaluación**
- id: UUID (Primary Key)
- application_id: UUID (Foreign Key)
- evaluator_id: UUID (Foreign Key)
- interview_id: UUID (Foreign Key) NULL
- type: ENUM('screening', 'technical', 'cultural', 'final')
- scores: JSON
- feedback: TEXT
- recommendation: ENUM('strong_yes', 'yes', 'maybe', 'no', 'strong_no')
- completed_at: TIMESTAMP
- created_at: TIMESTAMP

**7. Entrevista**
- id: UUID (Primary Key)
- application_id: UUID (Foreign Key)
- interviewer_ids: JSON
- scheduled_at: TIMESTAMP
- duration_minutes: INTEGER
- type: ENUM('phone', 'video', 'in_person', 'technical')
- meeting_link: VARCHAR(500)
- location: VARCHAR(255)
- status: ENUM('scheduled', 'completed', 'cancelled', 'no_show')
- notes: TEXT
- recording_url: VARCHAR(500)
- created_at: TIMESTAMP
- updated_at: TIMESTAMP

**8. Pipeline**
- id: UUID (Primary Key)
- company_id: UUID (Foreign Key)
- name: VARCHAR(255) NOT NULL
- stages: JSON
- is_default: BOOLEAN DEFAULT FALSE
- created_at: TIMESTAMP
- updated_at: TIMESTAMP

### Diagrama Entidad-Relación

erDiagram
    EMPRESA ||--o{ USUARIO : "emplea"
    EMPRESA ||--o{ VACANTE : "publica"
    EMPRESA ||--|| PIPELINE : "tiene"
    
    USUARIO ||--o{ VACANTE : "crea"
    USUARIO ||--o{ EVALUACION : "realiza"
    USUARIO ||--o{ ENTREVISTA : "participa"
    
    VACANTE ||--o{ APLICACION : "recibe"
    
    CANDIDATO ||--o{ APLICACION : "aplica"
    
    APLICACION ||--o{ EVALUACION : "tiene"
    APLICACION ||--o{ ENTREVISTA : "programa"
    
    ENTREVISTA ||--o{ EVALUACION : "genera"
    
    EMPRESA {
        UUID id PK
        VARCHAR name
        VARCHAR domain
        VARCHAR industry
        ENUM size
        ENUM subscription_plan
        VARCHAR billing_email
        TIMESTAMP created_at
        TIMESTAMP updated_at
    }
    
    USUARIO {
        UUID id PK
        VARCHAR email
        VARCHAR password_hash
        VARCHAR first_name
        VARCHAR last_name
        ENUM role
        UUID company_id FK
        BOOLEAN is_active
        TIMESTAMP created_at
        TIMESTAMP updated_at
    }
    
    VACANTE {
        UUID id PK
        VARCHAR title
        TEXT description
        JSON requirements
        DECIMAL salary_range_min
        DECIMAL salary_range_max
        VARCHAR location
        BOOLEAN remote_option
        ENUM employment_type
        ENUM experience_level
        ENUM status
        ENUM priority
        UUID created_by FK
        JSON assigned_recruiters
        JSON hiring_managers
        TIMESTAMP created_at
        TIMESTAMP updated_at
        TIMESTAMP deadline
    }
    
    CANDIDATO {
        UUID id PK
        VARCHAR email
        VARCHAR first_name
        VARCHAR last_name
        VARCHAR phone
        VARCHAR linkedin_url
        VARCHAR github_url
        VARCHAR portfolio_url
        VARCHAR location
        VARCHAR current_position
        VARCHAR current_company
        INTEGER experience_years
        JSON skills
        JSON education
        VARCHAR resume_url
        VARCHAR source
        DECIMAL ai_score
        TIMESTAMP created_at
        TIMESTAMP updated_at
    }
    
    APLICACION {
        UUID id PK
        UUID job_id FK
        UUID candidate_id FK
        ENUM status
        TIMESTAMP applied_at
        VARCHAR current_stage
        DECIMAL ai_compatibility_score
        TEXT recruiter_notes
        TEXT rejection_reason
        JSON offer_details
        TIMESTAMP created_at
        TIMESTAMP updated_at
    }
    
    EVALUACION {
        UUID id PK
        UUID application_id FK
        UUID evaluator_id FK
        UUID interview_id FK
        ENUM type
        JSON scores
        TEXT feedback
        ENUM recommendation
        TIMESTAMP completed_at
        TIMESTAMP created_at
    }
    
    ENTREVISTA {
        UUID id PK
        UUID application_id FK
        JSON interviewer_ids
        TIMESTAMP scheduled_at
        INTEGER duration_minutes
        ENUM type
        VARCHAR meeting_link
        VARCHAR location
        ENUM status
        TEXT notes
        VARCHAR recording_url
        TIMESTAMP created_at
        TIMESTAMP updated_at
    }
    
    PIPELINE {
        UUID id PK
        UUID company_id FK
        VARCHAR name
        JSON stages
        BOOLEAN is_default
        TIMESTAMP created_at
        TIMESTAMP updated_at
    }

## 4. Diseño de Alto Nivel

### Arquitectura del Sistema

El sistema LTI ATS está diseñado siguiendo una **arquitectura de microservicios en la nube** que prioriza la escalabilidad, mantenibilidad y rendimiento. La arquitectura se basa en principios de Domain-Driven Design (DDD) y utiliza patrones modernos como Event Sourcing y CQRS para casos específicos.

### Componentes Principales

**1. API Gateway**
- **Responsabilidades**: Enrutamiento de requests, autenticación, rate limiting, transformación de datos
- **Tecnología**: Kong o AWS API Gateway
- **Funciones**: Load balancing, SSL termination, request/response logging

**2. Servicio de Autenticación y Autorización**
- **Responsabilidades**: Gestión de usuarios, roles, permisos, JWT token management
- **Patrones**: OAuth 2.0, RBAC (Role-Based Access Control)
- **Integraciones**: SSO con Google, Microsoft, LinkedIn

**3. Servicio de Gestión de Vacantes**
- **Responsabilidades**: CRUD de job postings, workflow management, publishing a job boards
- **Base de datos**: PostgreSQL para datos relacionales
- **Cache**: Redis para consultas frecuentes

**4. Servicio de Gestión de Candidatos**
- **Responsabilidades**: Perfiles de candidatos, parsing de CVs, talent pool management
- **Integraciones**: LinkedIn API, parsing engines, background check services
- **Storage**: S3 para documentos (CVs, portfolios)

**5. Motor de IA y Machine Learning**
- **Responsabilidades**: Scoring de compatibilidad, matching algorithms, predictive analytics
- **Tecnologías**: Python/TensorFlow, MLflow para model management
- **Datos**: Data lake para training data, feature store

**6. Servicio de Comunicación**
- **Responsabilidades**: Email automation, notifications, chat en tiempo real
- **Integraciones**: SendGrid, Twilio, WebSocket para real-time features
- **Templates**: Biblioteca de plantillas personalizables

**7. Servicio de Analytics y Reporting**
- **Responsabilidades**: Métricas de negocio, dashboards, data export
- **Stack**: ELK Stack (Elasticsearch, Logstash, Kibana)
- **Visualización**: Embebido con herramientas como D3.js

**8. Servicio de Integraciones**
- **Responsabilidades**: Conectores con sistemas externos, webhooks, API management
- **Protocolos**: REST, GraphQL, webhooks
- **Sistemas**: HRIS, job boards, assessment tools

### Interacciones entre Componentes

**Flujo de Comunicación:**
1. **Síncrono**: REST APIs para operaciones CRUD inmediatas
2. **Asíncrono**: Message queues (RabbitMQ/Apache Kafka) para procesamiento en background
3. **Eventos**: Event bus para comunicación entre dominios
4. **Cache distribuido**: Redis Cluster para datos compartidos frecuentemente accedidos

**Patrones de Integración:**
- **API First**: Todos los servicios exponen APIs bien documentadas
- **Event-Driven**: Eventos de dominio para desacoplamiento
- **Circuit Breaker**: Resilencia ante fallos de servicios externos
- **Saga Pattern**: Para transacciones distribuidas complejas

### Diagrama de Arquitectura de Alto Nivel

graph TB
    subgraph "Frontend Layer"
        WEB[Web Application<br/>React/Next.js]
        MOBILE[Mobile App<br/>React Native]
        API_DOC[API Documentation<br/>Swagger/OpenAPI]
    end
    
    subgraph "API Gateway Layer"
        GATEWAY[API Gateway<br/>Kong/AWS API Gateway<br/>- Routing<br/>- Authentication<br/>- Rate Limiting<br/>- SSL Termination]
    end
    
    subgraph "Microservices Layer"
        AUTH[Authentication Service<br/>- User Management<br/>- JWT Tokens<br/>- OAuth 2.0<br/>- RBAC]
        
        JOBS[Job Management Service<br/>- Job CRUD<br/>- Workflow Engine<br/>- Publishing<br/>- Pipeline Management]
        
        CANDIDATES[Candidate Service<br/>- Profile Management<br/>- CV Parsing<br/>- Talent Pool<br/>- Search/Filter]
        
        AI[AI/ML Service<br/>- Scoring Algorithms<br/>- Matching Engine<br/>- Predictive Analytics<br/>- NLP Processing]
        
        COMM[Communication Service<br/>- Email Automation<br/>- Notifications<br/>- Real-time Chat<br/>- Templates]
        
        ANALYTICS[Analytics Service<br/>- Reporting<br/>- Dashboards<br/>- Data Export<br/>- KPI Tracking]
        
        INTEGRATIONS[Integration Service<br/>- External APIs<br/>- Webhooks<br/>- Data Sync<br/>- Third-party Connectors]
    end
    
    subgraph "Data Layer"
        POSTGRES[(PostgreSQL<br/>Primary Database)]
        REDIS[(Redis<br/>Cache & Sessions)]
        ELASTICSEARCH[(Elasticsearch<br/>Search & Analytics)]
        S3[(AWS S3<br/>File Storage)]
        KAFKA[Apache Kafka<br/>Event Streaming]
    end
    
    subgraph "External Systems"
        LINKEDIN[LinkedIn API]
        JOBBOARDS[Job Boards<br/>Indeed, Glassdoor]
        EMAIL[SendGrid/SES]
        HRIS[HRIS Systems]
        ASSESSMENT[Assessment Tools]
    end
    
    subgraph "Infrastructure"
        MONITOR[Monitoring<br/>Datadog/New Relic]
        LOGS[Logging<br/>ELK Stack]
        BACKUP[Backup Systems]
        CDN[CDN<br/>CloudFront]
    end
    
    WEB --> GATEWAY
    MOBILE --> GATEWAY
    API_DOC --> GATEWAY
    
    GATEWAY --> AUTH
    GATEWAY --> JOBS
    GATEWAY --> CANDIDATES
    GATEWAY --> AI
    GATEWAY --> COMM
    GATEWAY --> ANALYTICS
    GATEWAY --> INTEGRATIONS
    
    AUTH --> POSTGRES
    AUTH --> REDIS
    
    JOBS --> POSTGRES
    JOBS --> REDIS
    JOBS --> KAFKA
    
    CANDIDATES --> POSTGRES
    CANDIDATES --> S3
    CANDIDATES --> ELASTICSEARCH
    
    AI --> POSTGRES
    AI --> ELASTICSEARCH
    AI --> S3
    
    COMM --> REDIS
    COMM --> KAFKA
    
    ANALYTICS --> ELASTICSEARCH
    ANALYTICS --> POSTGRES
    
    INTEGRATIONS --> KAFKA
    INTEGRATIONS --> REDIS
    
    INTEGRATIONS --> LINKEDIN
    INTEGRATIONS --> JOBBOARDS
    COMM --> EMAIL
    INTEGRATIONS --> HRIS
    INTEGRATIONS --> ASSESSMENT
    
    MONITOR -.-> AUTH
    MONITOR -.-> JOBS
    MONITOR -.-> CANDIDATES
    MONITOR -.-> AI
    
    LOGS -.-> AUTH
    LOGS -.-> JOBS
    LOGS -.-> CANDIDATES
    LOGS -.-> AI

## 5. Diagrama C4 - Servicio de IA y Machine Learning

Para el diagrama C4, he seleccionado el **Motor de IA y Machine Learning** por ser el componente más innovador y diferenciador del sistema.

### Nivel 1: Contexto del Sistema

graph TB
    subgraph "Contexto del Sistema LTI ATS"
        RECRUITER[👤 Reclutador<br/>Busca candidatos óptimos<br/>y automatiza evaluaciones]
        
        HIRING_MANAGER[👤 Hiring Manager<br/>Evalúa candidatos<br/>y toma decisiones finales]
        
        HR_DIRECTOR[👤 HR Director<br/>Analiza métricas<br/>y optimiza procesos]
        
        CANDIDATE[👤 Candidato<br/>Aplica a posiciones<br/>y recibe feedback]
        
        LTI_SYSTEM[🏢 Sistema LTI ATS<br/>Plataforma inteligente de<br/>gestión de talento con IA]
        
        LINKEDIN[🔗 LinkedIn API<br/>Sourcing de candidatos<br/>y datos de perfil]
        
        JOB_BOARDS[🔗 Job Boards<br/>Indeed, Glassdoor<br/>Publicación de vacantes]
        
        HRIS[🔗 Sistemas HRIS<br/>Integración con datos<br/>de empleados]
        
        EMAIL_SERVICE[🔗 Email Service<br/>Comunicación automatizada<br/>con candidatos]
    end
    
    RECRUITER --> LTI_SYSTEM
    HIRING_MANAGER --> LTI_SYSTEM
    HR_DIRECTOR --> LTI_SYSTEM
    CANDIDATE --> LTI_SYSTEM
    
    LTI_SYSTEM --> LINKEDIN
    LTI_SYSTEM --> JOB_BOARDS
    LTI_SYSTEM --> HRIS
    LTI_SYSTEM --> EMAIL_SERVICE

### Nivel 2: Contenedores

graph TB
    subgraph "Sistema LTI ATS - Contenedores"
        WEB_APP[💻 Web Application<br/>React/Next.js<br/>Dashboard para reclutadores<br/>y hiring managers]
        
        API_GATEWAY[🌐 API Gateway<br/>Kong<br/>Routing, Authentication,<br/>Rate Limiting]
        
        AI_SERVICE[🤖 AI/ML Service<br/>Python/FastAPI<br/>Scoring, Matching,<br/>Predictive Analytics]
        
        CANDIDATE_SERVICE[👥 Candidate Service<br/>Node.js/Express<br/>Profile Management,<br/>CV Parsing]
        
        JOB_SERVICE[💼 Job Service<br/>Node.js/Express<br/>Job Management,<br/>Workflow Engine]
        
        POSTGRES_DB[(🗄️ PostgreSQL Database<br/>Primary data storage<br/>Jobs, Users, Applications)]
        
        REDIS_CACHE[(⚡ Redis Cache<br/>Session storage,<br/>Caching layer)]
        
        ML_DATA_LAKE[(🏞️ ML Data Lake<br/>AWS S3 + Parquet<br/>Training data,<br/>Feature store)]
        
        ELASTICSEARCH[(🔍 Elasticsearch<br/>Search engine,<br/>Analytics data)]
    end
    
    subgraph "Usuarios"
        RECRUITER[👤 Reclutador]
        HIRING_MANAGER[👤 Hiring Manager]
        CANDIDATE[👤 Candidato]
    end
    
    subgraph "Sistemas Externos"
        LINKEDIN_API[🔗 LinkedIn API]
        EMAIL_SERVICE[📧 SendGrid]
    end
    
    RECRUITER --> WEB_APP
    HIRING_MANAGER --> WEB_APP
    CANDIDATE --> WEB_APP
    
    WEB_APP --> API_GATEWAY
    
    API_GATEWAY --> AI_SERVICE
    API_GATEWAY --> CANDIDATE_SERVICE
    API_GATEWAY --> JOB_SERVICE
    
    AI_SERVICE --> ML_DATA_LAKE
    AI_SERVICE --> ELASTICSEARCH
    AI_SERVICE --> REDIS_CACHE
    
    CANDIDATE_SERVICE --> POSTGRES_DB
    CANDIDATE_SERVICE --> ELASTICSEARCH
    
    JOB_SERVICE --> POSTGRES_DB
    JOB_SERVICE --> REDIS_CACHE
    
    AI_SERVICE --> LINKEDIN_API
    CANDIDATE_SERVICE --> EMAIL_SERVICE

### Nivel 3: Componentes del AI/ML Service

graph TB
    subgraph "AI/ML Service - Componentes"
        API_CONTROLLER[🎛️ API Controller<br/>FastAPI Router<br/>Handles HTTP requests<br/>for AI operations]
        
        SCORING_ENGINE[🎯 Scoring Engine<br/>Candidate-Job matching<br/>Compatibility algorithms<br/>Multi-factor scoring]
        
        NLP_PROCESSOR[📝 NLP Processor<br/>Resume parsing<br/>Job description analysis<br/>Skill extraction]
        
        PREDICTION_ENGINE[🔮 Prediction Engine<br/>Success probability<br/>Time-to-hire forecasting<br/>Churn prediction]
        
        MODEL_MANAGER[🧠 Model Manager<br/>MLflow integration<br/>Model versioning<br/>A/B testing framework]
        
        FEATURE_STORE[🏪 Feature Store<br/>Feature engineering<br/>Real-time features<br/>Historical aggregations]
        
        TRAINING_PIPELINE[🚂 Training Pipeline<br/>Automated retraining<br/>Data validation<br/>Model evaluation]
        
        INFERENCE_CACHE[⚡ Inference Cache<br/>Prediction caching<br/>Performance optimization<br/>Response time SLA]
    end
    
    subgraph "External Dependencies"
        ML_DATA_LAKE[(🏞️ ML Data Lake)]
        REDIS_CACHE[(⚡ Redis Cache)]
        MONITORING[📊 Model Monitoring<br/>MLflow/Weights & Biases]
    end
    
    subgraph "Other Services"
        CANDIDATE_SERVICE[👥 Candidate Service]
        JOB_SERVICE[💼 Job Service]
        API_GATEWAY[🌐 API Gateway]
    end
    
    API_GATEWAY --> API_CONTROLLER
    
    API_CONTROLLER --> SCORING_ENGINE
    API_CONTROLLER --> NLP_PROCESSOR
    API_CONTROLLER --> PREDICTION_ENGINE
    
    SCORING_ENGINE --> FEATURE_STORE
    SCORING_ENGINE --> MODEL_MANAGER
    SCORING_ENGINE --> INFERENCE_CACHE
    
    NLP_PROCESSOR --> MODEL_MANAGER
    NLP_PROCESSOR --> FEATURE_STORE
    
    PREDICTION_ENGINE --> MODEL_MANAGER
    PREDICTION_ENGINE --> FEATURE_STORE
    PREDICTION_ENGINE --> INFERENCE_CACHE
    
    MODEL_MANAGER --> ML_DATA_LAKE
    MODEL_MANAGER --> MONITORING
    
    FEATURE_STORE --> ML_DATA_LAKE
    FEATURE_STORE --> REDIS_CACHE
    
    TRAINING_PIPELINE --> ML_DATA_LAKE
    TRAINING_PIPELINE --> MODEL_MANAGER
    TRAINING_PIPELINE --> MONITORING
    
    INFERENCE_CACHE --> REDIS_CACHE
    
    FEATURE_STORE --> CANDIDATE_SERVICE
    FEATURE_STORE --> JOB_SERVICE

### Nivel 4: Código - Scoring Engine (Componente Crítico)

# Scoring Engine - Arquitectura de Código

from abc import ABC, abstractmethod
from dataclasses import dataclass
from typing import Dict, List, Optional
import numpy as np
from sklearn.preprocessing import StandardScaler
from sklearn.ensemble import RandomForestRegressor

@dataclass
class ScoringRequest:
    """Request para scoring de candidato-trabajo"""
    candidate_id: str
    job_id: str
    candidate_features: Dict
    job_features: Dict
    context: Optional[Dict] = None

@dataclass 
class ScoringResult:
    """Resultado del scoring con explicabilidad"""
    overall_score: float
    component_scores: Dict[str, float]
    confidence: float
    explanation: List[str]
    recommendations: List[str]

class ScoringStrategy(ABC):
    """Strategy pattern para diferentes algoritmos de scoring"""
    
    @abstractmethod
    def calculate_score(self, request: ScoringRequest) -> ScoringResult:
        pass

class SkillMatchingScorer(ScoringStrategy):
    """Scorer especializado en matching de skills técnicas"""
    
    def __init__(self, skill_embeddings_model):
        self.skill_embeddings = skill_embeddings_model
        self.weight = 0.35
    
    def calculate_score(self, request: ScoringRequest) -> float:
        candidate_skills = request.candidate_features.get('skills', [])
        required_skills = request.job_features.get('required_skills', [])
        
        # Semantic similarity usando embeddings
        similarity_scores = []
        for req_skill in required_skills:
            best_match = max([
                self._calculate_semantic_similarity(req_skill, cand_skill)
                for cand_skill in candidate_skills
            ], default=0.0)
            similarity_scores.append(best_match)
        
        return np.mean(similarity_scores) if similarity_scores else 0.0
    
    def _calculate_semantic_similarity(self, skill1: str, skill2: str) -> float:
        # Implementación usando word embeddings o sentence transformers
        return self.skill_embeddings.similarity(skill1, skill2)

class ExperienceScorer(ScoringStrategy):
    """Scorer para experiencia y seniority"""
    
    def __init__(self):
        self.weight = 0.25
    
    def calculate_score(self, request: ScoringRequest) -> float:
        candidate_exp = request.candidate_features.get('years_experience', 0)
        required_exp = request.job_features.get('min_experience', 0)
        ideal_exp = request.job_features.get('ideal_experience', required_exp + 2)
        
        if candidate_exp < required_exp:
            # Penalización por falta de experiencia
            return max(0, 1 - (required_exp - candidate_exp) * 0.2)
        elif candidate_exp <= ideal_exp:
            # Zona óptima
            return 1.0
        else:
            # Sobrecualificación - ligera penalización
            excess = candidate_exp - ideal_exp
            return max(0.7, 1 - excess * 0.05)

class CulturalFitScorer(ScoringStrategy):
    """Scorer para ajuste cultural usando ML"""
    
    def __init__(self, model_manager):
        self.weight = 0.20
        self.model = model_manager.get_model('cultural_fit_v2')
    
    def calculate_score(self, request: ScoringRequest) -> float:
        # Features para el modelo de cultural fit
        features = self._extract_cultural_features(request)
        prediction = self.model.predict_proba([features])[0]
        return prediction[1]  # Probabilidad de buen fit
    
    def _extract_cultural_features(self, request: ScoringRequest) -> List[float]:
        # Extracción de features relevantes para cultura
        candidate = request.candidate_features
        job = request.job_features
        
        return [
            candidate.get('remote_preference', 0.5),
            candidate.get('team_size_preference', 5) / 10,
            candidate.get('growth_orientation', 0.5),
            job.get('team_collaboration_score', 0.5),
            job.get('innovation_score', 0.5),
            # ... más features
        ]

class LocationScorer(ScoringStrategy):
    """Scorer para compatibilidad geográfica"""
    
    def __init__(self, geo_service):
        self.weight = 0.20
        self.geo_service = geo_service
    
    def calculate_score(self, request: ScoringRequest) -> float:
        candidate_location = request.candidate_features.get('location')
        job_location = request.job_features.get('location')
        remote_option = request.job_features.get('remote_option', False)
        
        if remote_option:
            return 1.0
        
        if not candidate_location or not job_location:
            return 0.5  # Score neutro si falta información
        
        distance = self.geo_service.calculate_distance(
            candidate_location, job_location
        )
        
        # Función de decaimiento exponencial
        return np.exp(-distance / 50)  # 50km como distancia de referencia

class CompositeScoringEngine:
    """Engine principal que combina múltiples scorers"""
    
    def __init__(self, feature_store, model_manager):
        self.feature_store = feature_store
        self.model_manager = model_manager
        
        # Inicializar scorers individuales
        self.scorers = [
            SkillMatchingScorer(model_manager.get_model('skill_embeddings')),
            ExperienceScorer(),
            CulturalFitScorer(model_manager),
            LocationScorer(feature_store.geo_service)
        ]
        
        # Meta-modelo para combinar scores optimalmente
        self.meta_model = model_manager.get_model('score_combiner_v1')
    
    def score_candidate(self, request: ScoringRequest) -> ScoringResult:
        """Scoring principal con explicabilidad"""
        
        # Calcular scores individuales
        component_scores = {}
        for scorer in self.scorers:
            scorer_name = scorer.__class__.__name__
            component_scores[scorer_name] = scorer.calculate_score(request)
        
        # Combinar usando meta-modelo entrenado
        features = list(component_scores.values())
        overall_score = self.meta_model.predict([features])[0]
        confidence = self._calculate_confidence(component_scores)
        
        # Generar explicaciones
        explanation = self._generate_explanation(component_scores, request)
        recommendations = self._generate_recommendations(component_scores, request)
        
        return ScoringResult(
            overall_score=float(overall_score),
            component_scores=component_scores,
            confidence=confidence,
            explanation=explanation,
            recommendations=recommendations
        )
    
    def _calculate_confidence(self, scores: Dict[str, float]) -> float:
        """Calcula confianza basada en consistencia de scores"""
        values = list(scores.values())
        std_dev = np.std(values)
        mean_score = np.mean(values)
        
        # Confianza alta cuando los scores son consistentes
        consistency_score = 1 - min(std_dev / 0.5, 1.0)
        
        # Confianza también depende del score promedio
        score_confidence = mean_score
        
        return (consistency_score + score_confidence) / 2
    
    def _generate_explanation(self, scores: Dict, request: ScoringRequest) -> List[str]:
        """Genera explicaciones human-readable"""
        explanations = []
        
        # Identificar fortalezas y debilidades
        sorted_scores = sorted(scores.items(), key=lambda x: x[1], reverse=True)
        
        best_aspect = sorted_scores[0]
        explanations.append(f"Fortaleza principal: {best_aspect[0]} (score: {best_aspect[1]:.2f})")
        
        worst_aspect = sorted_scores[-1]
        if worst_aspect[1] < 0.6:
            explanations.append(f"Área de mejora: {worst_aspect[0]} (score: {worst_aspect[1]:.2f})")
        
        return explanations
    
    def _generate_recommendations(self, scores: Dict, request: ScoringRequest) -> List[str]:
        """Genera recomendaciones actionables"""
        recommendations = []
        
        if scores.get('SkillMatchingScorer', 0) < 0.7:
            recommendations.append("Considerar entrevista técnica adicional")
        
        if scores.get('CulturalFitScorer', 0) < 0.6:
            recommendations.append("Incluir team lead en proceso de entrevistas")
        
        return recommendations

# Factory para crear diferentes tipos de scoring engines
class ScoringEngineFactory:
    """Factory para crear engines específicos por industria/role"""
    
    @staticmethod
    def create_engine(job_type: str, feature_store, model_manager):
        if job_type == 'tech':
            return TechScoringEngine(feature_store, model_manager)
        elif job_type == 'sales':
            return SalesScoringEngine(feature_store, model_manager)
        else:
            return CompositeScoringEngine(feature_store, model_manager)

# Ejemplo de engine especializado
class TechScoringEngine(CompositeScoringEngine):
    """Engine especializado para roles técnicos"""
    
    def __init__(self, feature_store, model_manager):
        super().__init__(feature_store, model_manager)
        
        # Weights específicos para tech roles
        self.scorers[0].weight = 0.50  # Skills matching más importante
        self.scorers[1].weight = 0.30  # Experience
        self.scorers[2].weight = 0.10  # Cultural fit menos crítico
        self.scorers[3].weight = 0.10  # Location
        
        # Agregar scorer específico para tech
        self.scorers.append(
            TechnicalAssessmentScorer(model_manager)
        )

class TechnicalAssessmentScorer(ScoringStrategy):
    """Scorer para evaluaciones técnicas automatizadas"""
    
    def __init__(self, model_manager):
        self.weight = 0.25
        self.code_analysis_model = model_manager.get_model('code_quality_v1')
    
    def calculate_score(self, request: ScoringRequest) -> float:
        # Análisis de GitHub, coding challenges, etc.
        github_score = self._analyze_github_profile(request.candidate_features)
        assessment_score = self._analyze_technical_assessment(request.candidate_features)
        
        return (github_score + assessment_score) / 2
    
    def _analyze_github_profile(self, candidate_features: Dict) -> float:
        github_url = candidate_features.get('github_url')
        if not github_url:
            return 0.5  # Neutro si no hay GitHub
        
        # Análisis de commits, languages, project quality
        github_data = candidate_features.get('github_analysis', {})
        return github_data.get('quality_score', 0.5)
    
    def _analyze_technical_assessment(self, candidate_features: Dict) -> float:
        assessment_results = candidate_features.get('technical_assessment', {})
        return assessment_results.get('normalized_score', 0.5)

## Resumen Ejecutivo

El sistema **LTI ATS** representa una solución innovadora en el mercado de HR Tech que combina las mejores prácticas de arquitectura de software moderna con capacidades avanzadas de inteligencia artificial. El diseño propuesto aborda los principales pain points del reclutamiento actual:

### Principales Fortalezas del Diseño:

**1. Arquitectura Escalable y Resiliente**
- Microservicios desacoplados que permiten escalamiento independiente
- Patrones de resilencia (Circuit Breaker, Event Sourcing) para alta disponibilidad
- Infraestructura cloud-native preparada para crecimiento exponencial

**2. Diferenciación Competitiva Clara**
- Motor de IA propietario con scoring multi-dimensional explicable
- Colaboración en tiempo real entre stakeholders
- Automatización inteligente que aprende y mejora continuamente

**3. Experiencia del Usuario Optimizada**
- Interfaces diseñadas específicamente para cada tipo de usuario
- Flujos de trabajo intuitivos que reducen la curva de aprendizaje
- Portal del candidato que mejora significativamente la experiencia de aplicación

**4. Modelo de Negocio Sostenible**
- Múltiples flujos de ingresos (SaaS, servicios, integraciones premium)
- Métricas claras de éxito y retención
- Escalabilidad del modelo desde startups hasta enterprise

### Consideraciones de Implementación:

**Fase 1 (MVP - 6 meses):**
- Core ATS functionality (gestión de vacantes y candidatos)
- Scoring básico con IA
- Dashboard colaborativo fundamental

**Fase 2 (Growth - 6-12 meses):**
- Motor de IA completo con ML pipeline
- Integraciones principales (LinkedIn, job boards)
- Analytics avanzados

**Fase 3 (Scale - 12+ meses):**
- Automatización completa de workflows
- AI conversacional
- Expansión internacional

El diseño presentado proporciona una base sólida para construir el ATS del futuro, con una arquitectura que soporta tanto las necesidades actuales como la evolución futura del mercado de reclutamiento. La combinación de tecnología avanzada, experiencia de usuario superior y modelo de negocio robusto posiciona a LTI para capturar una participación significativa en el mercado de HR Tech.