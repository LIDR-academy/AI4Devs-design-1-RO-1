# Diagrama C4 - User Service (Completo) - PlantUML

## 🎯 Componente Seleccionado: User Service

**Justificación:** El User Service es el **más sencillo** pero **fundamental** del sistema. Maneja autenticación, gestión de usuarios y perfiles, con lógica de negocio clara y dependencias mínimas.

---

## 📊 Nivel 1: System Context Diagram

```plantuml
@startuml C4_Context
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Context.puml

LAYOUT_WITH_LEGEND()

title System Context Diagram - LTI ATS Platform

Person(recruiter, "Recruiter", "HR professional who manages candidates and job postings")
Person(hiring_manager, "Hiring Manager", "Manager who reviews candidates and makes hiring decisions")
Person(admin, "System Admin", "Manages company settings and user permissions")

System(lti_ats, "LTI ATS Platform", "Applicant Tracking System with AI-powered matching and collaboration")

System_Ext(google_workspace, "Google Workspace", "Calendar and authentication services")
System_Ext(linkedin, "LinkedIn", "Professional networking and job posting platform")
System_Ext(email_service, "Email Service", "SendGrid for transactional emails")
System_Ext(slack, "Slack", "Team communication and notifications")

Rel(recruiter, lti_ats, "Manages candidates, posts jobs, schedules interviews")
Rel(hiring_manager, lti_ats, "Reviews candidates, provides feedback, makes decisions")
Rel(admin, lti_ats, "Configures system, manages users, views analytics")

Rel(lti_ats, google_workspace, "Syncs calendars, authenticates users")
Rel(lti_ats, linkedin, "Posts jobs, imports candidate profiles")
Rel(lti_ats, email_service, "Sends notifications and communications")
Rel(lti_ats, slack, "Sends real-time notifications")

@enduml
```

---

## 📊 Nivel 2: Container Diagram

```plantuml
@startuml C4_Container
!define C4_CONTAINER_BG_COLOR #1168bd
!define C4_PERSON_BG_COLOR #08427b
!define C4_SYSTEM_BG_COLOR #1168bd
!define C4_CONTAINER_DB_BG_COLOR #23a2d6

skinparam rectangle {
    FontColor white
    BorderColor black
    BorderThickness 2
}

skinparam person {
    FontColor white
    BorderColor black
    BorderThickness 2
}

title Container Diagram - LTI ATS Platform

rectangle "LTI Users\n[Person]\nRecruiters, Hiring Managers, Admins" as users #08427b

package "LTI ATS Platform" {
    rectangle "Web Application\n[Container: React, TypeScript]\nProvides user interface for recruitment management" as web_app #1168bd
    rectangle "Mobile App\n[Container: React Native]\nMobile interface for on-the-go recruitment tasks" as mobile_app #1168bd
    rectangle "API Gateway\n[Container: Kong]\nRoutes requests, handles authentication, rate limiting" as api_gateway #1168bd
    
    rectangle "User Service\n[Container: NestJS, TypeScript]\nHandles user authentication, profiles, and permissions" as user_service #1168bd
    rectangle "Job Service\n[Container: NestJS, TypeScript]\nManages job postings and applications" as job_service #1168bd
    rectangle "Candidate Service\n[Container: NestJS, TypeScript]\nManages candidate profiles and CVs" as candidate_service #1168bd
    rectangle "AI Service\n[Container: Python, FastAPI]\nProvides AI matching and content generation" as ai_service #1168bd
    rectangle "Notification Service\n[Container: NestJS, TypeScript]\nHandles email and push notifications" as notification_service #1168bd
    
    database "User Database\n[Database: PostgreSQL]\nStores user accounts, companies, roles" as user_db #23a2d6
    database "Main Database\n[Database: PostgreSQL]\nStores jobs, candidates, applications" as main_db #23a2d6
    database "Cache\n[Database: Redis]\nCaches user sessions and frequent data" as cache #23a2d6
    database "Search Database\n[Database: Elasticsearch]\nIndexes searchable content" as search_db #23a2d6
}

rectangle "Google Workspace\n[External System]\nCalendar and authentication" as google_workspace #999999
rectangle "Email Provider\n[External System]\nSendGrid" as email_provider #999999

users --> web_app : "Uses\n[HTTPS]"
users --> mobile_app : "Uses\n[HTTPS]"

web_app --> api_gateway : "Makes API calls\n[HTTPS/REST]"
mobile_app --> api_gateway : "Makes API calls\n[HTTPS/REST]"

api_gateway --> user_service : "Routes requests\n[HTTP/REST]"
api_gateway --> job_service : "Routes requests\n[HTTP/REST]"
api_gateway --> candidate_service : "Routes requests\n[HTTP/REST]"

user_service --> user_db : "Reads/Writes\n[SQL/TCP]"
user_service --> cache : "Caches sessions\n[Redis Protocol]"
job_service --> main_db : "Reads/Writes\n[SQL/TCP]"
candidate_service --> main_db : "Reads/Writes\n[SQL/TCP]"
candidate_service --> search_db : "Indexes profiles\n[HTTP/REST]"

user_service --> google_workspace : "OAuth authentication\n[HTTPS/OAuth2]"
notification_service --> email_provider : "Sends emails\n[HTTPS/API]"

@enduml
```

---

## 📊 Nivel 3: Component Diagram - User Service

```plantuml
@startuml C4_Component_UserService
!theme plain
title Component Diagram - User Service

skinparam rectangle {
    BackgroundColor lightblue
    BorderColor black
    FontSize 10
}

skinparam database {
    BackgroundColor lightgreen
    BorderColor black
}

skinparam cloud {
    BackgroundColor lightyellow
    BorderColor black
}

rectangle "API Gateway\n[Container: Kong]\nAPI routing and security" as api_gateway #dddddd

package "User Service" {
    ' Controllers Layer
    rectangle "Auth Controller\n[Component: NestJS]\nHandles login, logout, password reset" as auth_controller
    rectangle "User Controller\n[Component: NestJS]\nManages user CRUD operations" as user_controller
    rectangle "Profile Controller\n[Component: NestJS]\nManages user profiles and preferences" as profile_controller
    rectangle "Company Controller\n[Component: NestJS]\nManages company settings" as company_controller
    
    ' Services Layer
    rectangle "Authentication Service\n[Component: NestJS]\nBusiness logic for authentication" as auth_service
    rectangle "User Management Service\n[Component: NestJS]\nBusiness logic for user management" as user_service_logic
    rectangle "Profile Service\n[Component: NestJS]\nBusiness logic for profiles" as profile_service
    rectangle "Company Service\n[Component: NestJS]\nBusiness logic for companies" as company_service
    rectangle "Permission Service\n[Component: NestJS]\nRole-based access control" as permission_service
    
    ' Repository Layer
    rectangle "User Repository\n[Component: TypeORM]\nData access for users" as user_repository
    rectangle "Company Repository\n[Component: TypeORM]\nData access for companies" as company_repository
    rectangle "Session Repository\n[Component: Redis]\nSession management" as session_repository
    
    ' Utilities
    rectangle "JWT Strategy\n[Component: Passport]\nJWT token validation" as jwt_strategy
    rectangle "OAuth Strategy\n[Component: Passport]\nGoogle OAuth integration" as oauth_strategy
    rectangle "Password Hasher\n[Component: bcrypt]\nPassword encryption" as password_hasher
    rectangle "Email Validator\n[Component: Utility]\nEmail format validation" as email_validator
}

database "User Database\n[Database: PostgreSQL]\nUser and company data" as user_db
database "Redis Cache\n[Database: Redis]\nSessions and cache" as cache
cloud "Google OAuth\n[External System]\nOAuth2 provider" as google_oauth
cloud "Email Service\n[External System]\nSendGrid" as email_service

' External to Controllers
api_gateway --> auth_controller : "Routes auth requests\n[HTTP/REST]"
api_gateway --> user_controller : "Routes user requests\n[HTTP/REST]"
api_gateway --> profile_controller : "Routes profile requests\n[HTTP/REST]"
api_gateway --> company_controller : "Routes company requests\n[HTTP/REST]"

' Controllers to Services
auth_controller --> auth_service : "Calls\n[Method]"
user_controller --> user_service_logic : "Calls\n[Method]"
profile_controller --> profile_service : "Calls\n[Method]"
company_controller --> company_service : "Calls\n[Method]"

' Service to Service
auth_service --> permission_service : "Validates permissions\n[Method]"
user_service_logic --> permission_service : "Checks roles\n[Method]"
profile_service --> user_service_logic : "Gets user data\n[Method]"

' Services to Repositories
auth_service --> user_repository : "Validates credentials\n[Method]"
auth_service --> session_repository : "Manages sessions\n[Method]"
user_service_logic --> user_repository : "CRUD operations\n[Method]"
profile_service --> user_repository : "Updates profiles\n[Method]"
company_service --> company_repository : "CRUD operations\n[Method]"

' Services to Utilities
auth_service --> jwt_strategy : "Generates tokens\n[Method]"
auth_service --> oauth_strategy : "OAuth flow\n[Method]"
auth_service --> password_hasher : "Hashes passwords\n[Method]"
user_service_logic --> email_validator : "Validates emails\n[Method]"

' Repositories to Databases
user_repository --> user_db : "Queries\n[SQL/TCP]"
company_repository --> user_db : "Queries\n[SQL/TCP]"
session_repository --> cache : "Stores sessions\n[Redis Protocol]"

' External integrations
oauth_strategy --> google_oauth : "OAuth flow\n[HTTPS/OAuth2]"
auth_service --> email_service : "Password reset emails\n[HTTPS/API]"

@enduml
```

---

## 📊 Nivel 4: Code Diagram - Authentication Service

```plantuml
@startuml AuthService_Basic
title Authentication Service Internal Structure

class AuthService {
    login()
    register()
    oauthLogin()
    logout()
    validateToken()
    refreshToken()
    resetPassword()
    changePassword()
}

class UserRepository {
    findByEmail()
    create()
    updatePassword()
}

class TokenGenerator {
    generateTokens()
    verifyToken()
    refreshToken()
}

class SessionRepository {
    storeSession()
    removeSession()
}

class PasswordValidator {
    validate()
}

class RateLimiter {
    checkAttempts()
}

class EmailService {
    sendWelcomeEmail()
    sendResetEmail()
}

AuthService --> UserRepository
AuthService --> TokenGenerator
AuthService --> SessionRepository
AuthService --> PasswordValidator
AuthService --> RateLimiter
AuthService --> EmailService

@enduml
```

---

## 🔍 Explicación Detallada por Niveles

### **Nivel 1: System Context**
- **Scope:** Todo el sistema LTI ATS desde perspectiva externa
- **Audiencia:** Stakeholders de negocio, arquitectos de solución
- **Propósito:** Entender qué hace el sistema y cómo interactúa con usuarios y sistemas externos

### **Nivel 2: Container**
- **Scope:** Dentro del sistema LTI, mostrando contenedores de alto nivel
- **Audiencia:** Arquitectos de software, desarrolladores senior
- **Propósito:** Decisiones de tecnología y comunicación entre contenedores

### **Nivel 3: Component (User Service)**
- **Scope:** Dentro del User Service, mostrando componentes principales
- **Audiencia:** Desarrolladores del equipo User Service
- **Propósito:** Estructura interna del servicio y responsabilidades

### **Nivel 4: Code (Authentication Service)**
- **Scope:** Dentro del Authentication Service, mostrando clases y métodos
- **Audiencia:** Desarrolladores trabajando en autenticación
- **Propósito:** Implementación detallada y flujo de código

---

## 🛠️ Implementación Real - Snippets de Código

### **Authentication Service (TypeScript)**

```typescript
@Injectable()
export class AuthService {
  constructor(
    private userRepository: UserRepository,
    private sessionRepository: SessionRepository,
    private tokenGenerator: TokenGenerator,
    private passwordHasher: PasswordHasher,
    private emailService: EmailService,
    private rateLimiter: RateLimiter
  ) {}

  async login(email: string, password: string, ip: string): Promise<LoginResponse> {
    // Rate limiting
    await this.rateLimiter.checkLoginAttempts(ip, email);
    
    // Find user
    const user = await this.userRepository.findByEmail(email);
    if (!user) {
      throw new UnauthorizedException('Invalid credentials');
    }
    
    // Verify password
    const isValidPassword = await this.passwordHasher.verify(password, user.passwordHash);
    if (!isValidPassword) {
      await this.rateLimiter.recordFailedAttempt(ip, email);
      throw new UnauthorizedException('Invalid credentials');
    }
    
    // Generate tokens
    const tokens = await this.tokenGenerator.generateTokens(user);
    
    // Store session
    await this.sessionRepository.storeSession(user.id, tokens.refreshToken, ip);
    
    // Reset rate limiting
    await this.rateLimiter.resetAttempts(ip, email);
    
    return {
      accessToken: tokens.accessToken,
      refreshToken: tokens.refreshToken,
      user: this.sanitizeUser(user)
    };
  }

  async register(userData: RegisterDto): Promise<RegisterResponse> {
    // Validate password strength
    await this.passwordValidator.validate(userData.password);
    
    // Check if user exists
    const existingUser = await this.userRepository.findByEmail(userData.email);
    if (existingUser) {
      throw new ConflictException('User already exists');
    }
    
    // Hash password
    const passwordHash = await this.passwordHasher.hash(userData.password);
    
    // Create user
    const user = await this.userRepository.create({
      ...userData,
      passwordHash,
      isActive: true,
      emailVerified: false
    });
    
    // Send welcome email
    await this.emailService.sendWelcomeEmail(user.email, user.firstName);
    
    return {
      message: 'User registered successfully',
      userId: user.id
    };
  }

  async oauthLogin(oauthData: OAuthUserData): Promise<LoginResponse> {
    // Find or create user
    let user = await this.userRepository.findByEmail(oauthData.email);
    
    if (!user) {
      user = await this.userRepository.create({
        email: oauthData.email,
        firstName: oauthData.firstName,
        lastName: oauthData.lastName,
        avatarUrl: oauthData.picture,
        isActive: true,
        emailVerified: true,
        oauthProvider: oauthData.provider,
        oauthId: oauthData.id
      });
    }
    
    // Generate tokens
    const tokens = await this.tokenGenerator.generateTokens(user);
    
    // Store session
    await this.sessionRepository.storeSession(user.id, tokens.refreshToken);
    
    return {
      accessToken: tokens.accessToken,
      refreshToken: tokens.refreshToken,
      user: this.sanitizeUser(user)
    };
  }
}
```

### **Database Schema (User Service)**

```sql
-- Users table
CREATE TABLE users (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    company_id UUID NOT NULL REFERENCES companies(id),
    email VARCHAR(255) UNIQUE NOT NULL,
    password_hash VARCHAR(255),
    first_name VARCHAR(100) NOT NULL,
    last_name VARCHAR(100) NOT NULL,
    role VARCHAR(50) NOT NULL DEFAULT 'recruiter',
    phone VARCHAR(20),
    avatar_url VARCHAR(500),
    oauth_provider VARCHAR(50),
    oauth_id VARCHAR(100),
    permissions JSONB DEFAULT '{}',
    preferences JSONB DEFAULT '{}',
    email_verified BOOLEAN DEFAULT FALSE,
    last_login TIMESTAMP,
    created_at TIMESTAMP DEFAULT NOW(),
    updated_at TIMESTAMP DEFAULT NOW(),
    is_active BOOLEAN DEFAULT TRUE
);

-- Companies table
CREATE TABLE companies (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    name VARCHAR(255) NOT NULL,
    industry VARCHAR(100),
    description TEXT,
    website VARCHAR(255),
    logo_url VARCHAR(500),
    timezone VARCHAR(50) DEFAULT 'UTC',
    language VARCHAR(10) DEFAULT 'en',
    settings JSONB DEFAULT '{}',
    created_at TIMESTAMP DEFAULT NOW(),
    updated_at TIMESTAMP DEFAULT NOW(),
    is_active BOOLEAN DEFAULT TRUE
);

-- Sessions table (Redis structure)
-- Key: session:{userId}:{sessionId}
-- Value: { refreshToken, ip, userAgent, expiresAt }
```

---

## 🚀 Cómo Crear las Imágenes

### **Para PlantUML C4:**

1. **Ve a:** http://www.plantuml.com/plantuml/uml/
2. **Copia cada diagrama** (uno a la vez) del código PlantUML
3. **Se genera automáticamente** la imagen
4. **Descarga** haciendo clic derecho → "Guardar imagen"

### **Alternativa con Visual Studio Code:**
1. **Instala** la extensión "PlantUML"
2. **Crea archivo** `.puml` con el código
3. **Ctrl+Shift+P** → "PlantUML: Preview Current Diagram"
4. **Exporta** como PNG/SVG

---

## 📋 **Ventajas del User Service para C4:**

✅ **Sencillo pero completo** - Lógica clara sin complejidad excesiva  
✅ **Bien definido** - Responsabilidades claras y límites precisos  
✅ **Pocas dependencias** - Solo DB, cache y servicios externos básicos  
✅ **Patrones conocidos** - CRUD, autenticación, autorización  
✅ **Fácil de entender** - Perfecto para demostrar la metodología C4  

¿Te gustaría que profundice en algún nivel específico o que añada más detalles de implementación?