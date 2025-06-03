# Sistema de Gestión de Candidatos LTI - Entregable 4

## 📋 Descripción del Software LTI

### ¿Qué es LTI?

**LTI (Leading Talent Intelligence)** es un sistema ATS (Applicant Tracking System) de nueva generación que revoluciona la gestión de candidatos mediante inteligencia artificial, colaboración en tiempo real y automatización inteligente. Diseñado para departamentos de Recursos Humanos modernos que buscan eficiencia, precisión y una experiencia de usuario excepcional.

### 🎯 Valor Añadido y Ventajas Competitivas

**Diferenciadores clave:**

1. **🧠 IA Generativa Avanzada**
   - Match semántico inteligente entre CVs y ofertas laborales
   - Generación automática de feedback post-entrevista
   - Redacción automática de emails personalizados
   - Predicciones de éxito y tiempo de contratación

2. **⚡ Colaboración en Tiempo Real**
   - Comentarios y menciones instantáneas estilo Slack
   - Asignación de tareas colaborativas
   - Historial de actividad en vivo
   - Notificaciones inteligentes

3. **🔗 Integración 360°**
   - Conexión nativa con LinkedIn, Indeed, Google Calendar, Zoom
   - Sincronización automática con HackerRank, Codility
   - APIs robustas para herramientas corporativas

4. **📊 Analytics Predictivos**
   - KPIs en tiempo real con insights automáticos
   - Dashboards interactivos y personalizables
   - Reportes de rendimiento por reclutador y fuente

5. **🌐 Experiencia Multicanal**
   - Interfaz responsive optimizada para móviles
   - Soporte multilenguaje con detección automática de zona horaria
   - UX intuitiva diseñada para velocidad de contratación

### 🚀 Funciones Principales

**Gestión de Ofertas:**
- Creación y publicación automatizada en múltiples portales
- Asignación de responsables y configuración de pipelines personalizados

**Gestión de Candidatos:**
- Ingesta automática desde múltiples fuentes (email, portales, referidos)
- Perfiles enriquecidos con historial completo de interacciones

**Proceso de Selección:**
- Coordinación de entrevistas con integración calendario
- Aplicación de pruebas técnicas automatizadas
- Evaluaciones colaborativas con IA

**Comunicación Inteligente:**
- Templates de email con generación automática por IA
- Seguimiento personalizado de candidatos
- Notificaciones contextuales

**Reportes y KPIs:**
- Métricas de embudo por posición y reclutador
- Análisis de fuentes más efectivas
- Predicciones de tiempo de cierre

---

## 📊 Lean Canvas - Modelo de Negocio LTI

| **Problema** | **Segmento de Clientes** | **Propuesta de Valor Única** |
|--------------|-------------------------|-------------------------------|
| • Procesos de reclutamiento lentos e ineficientes<br>• Falta de colaboración entre equipos de HR<br>• Pérdida de candidatos por mala experiencia<br>• Decisiones basadas en intuición, no datos<br>• Herramientas fragmentadas y costosas | **Primario:**<br>• Startups y scale-ups (50-500 empleados)<br>• Departamentos de HR modernos<br><br>**Secundario:**<br>• Empresas medianas en transformación digital<br>• Consultoras de recruiting | **"El único ATS que combina IA generativa, colaboración en tiempo real y analytics predictivos para reducir el tiempo de contratación en un 40%"** |

| **Solución** | **Canales** | **Flujo de Ingresos** |
|--------------|-------------|----------------------|
| • Plataforma todo-en-uno con IA integrada<br>• Automatización inteligente de tareas repetitivas<br>• Interfaz colaborativa en tiempo real<br>• Integraciones nativas con herramientas populares<br>• Analytics y reportes predictivos | • Marketing digital (SEO, SEM, content marketing)<br>• Partnerships con consultoras de HR<br>• Eventos y conferencias del sector<br>• Programa de referidos<br>• Sales directo (inside sales) | **SaaS por suscripción:**<br>• Plan Starter: $49/mes (hasta 5 usuarios)<br>• Plan Professional: $99/mes (hasta 15 usuarios)<br>• Plan Enterprise: $199/mes (usuarios ilimitados)<br><br>**Adicionales:**<br>• Setup y migración: $500-2000<br>• Integraciones custom: $200/mes |

| **Estructura de Costos** | **Métricas Clave** | **Ventaja Competitiva** |
|-------------------------|-------------------|------------------------|
| **Fijos:**<br>• Desarrollo y mantenimiento de software<br>• Infraestructura cloud (AWS/Azure)<br>• Equipo de desarrollo y soporte<br><br>**Variables:**<br>• APIs de IA (OpenAI, etc.)<br>• Integraciones de terceros<br>• Marketing y adquisición de clientes | • **Acquisition:** CAC < $200<br>• **Retention:** Churn < 5% mensual<br>• **Growth:** MRR growth > 15%<br>• **Usage:** Time-to-hire reduction > 30%<br>• **Satisfaction:** NPS > 50 | • **Tecnológica:** IA generativa aplicada específicamente a recruiting<br>• **Experiencia:** Interfaz colaborativa única en el mercado<br>• **Integraciones:** Ecosistema más completo que competidores<br>• **Datos:** Analytics predictivos basados en ML |

---

## 🏗️ Arquitectura del Sistema

### Stack Tecnológico

**Frontend:**
- React 18 + Vite
- TailwindCSS + ShadCN/UI
- TypeScript
- React Query para state management
- i18next para multilenguaje

**Backend:**
- NestJS (Node.js)
- Prisma ORM
- PostgreSQL
- Redis para caching
- WebSockets para tiempo real

**Integraciones:**
- OpenAI API (GPT-4) para IA generativa
- Google Calendar/Outlook APIs
- LinkedIn/Indeed APIs
- Zoom/Meet SDKs
- SendGrid para emails

**Infraestructura:**
- AWS/Azure Cloud
- Docker containers
- CI/CD con GitHub Actions
- Monitoring con DataDog

### Modelo de Datos Clave

**Entidades Principales:**
- `Users` (Reclutadores, Hiring Managers)
- `Companies` (Organizaciones)
- `Jobs` (Ofertas laborales)
- `Candidates` (Candidatos)
- `Applications` (Aplicaciones)
- `Interviews` (Entrevistas)
- `Evaluations` (Evaluaciones)
- `Tasks` (Tareas colaborativas)
- `AI_Matches` (Matches de IA)
- `Communications` (Historial de comunicaciones)

---

## 📝 Conclusión

Este diseño establece las bases para un ATS moderno que combina eficiencia operativa, colaboración inteligente y automatización avanzada, posicionando a LTI como líder en la transformación digital del reclutamiento.

**Próximos pasos:**
1. Definición detallada del modelo de datos
2. Diseño de la arquitectura de microservicios
3. Prototipado de la interfaz de usuario
4. Plan de implementación por fases
5. Estrategia de go-to-market