# Historia de Usuario Épica: Gestión Integral de Candidatos (ATS LTI)

## Como
Reclutador o Hiring Manager de una empresa con procesos activos de contratación,

## Quiero
una plataforma centralizada y colaborativa para gestionar el ciclo completo de reclutamiento, incluyendo:

- Publicación de ofertas laborales en múltiples canales
- Gestión de candidatos de múltiples orígenes (aplicaciones directas, referidos, importaciones, portales externos como LinkedIn/Indeed)
- Revisión y seguimiento del avance de cada candidato por etapa
- Organización de entrevistas (presenciales, remotas o mixtas) integradas con Zoom, Meet y calendarios externos (Google/Outlook)
- Aplicación de pruebas técnicas mediante plataformas de terceros (HackerRank, Codility, etc.)
- Comunicación efectiva con los candidatos a través de email o Slack
- Colaboración en tiempo real con otros miembros del equipo mediante comentarios, asignación de tareas y menciones
- Uso de inteligencia artificial para:
  - Match semántico entre candidatos y posiciones
  - Generación automática de feedback post-entrevista
  - Redacción automática de emails y comunicaciones
  - Predicción de éxito y tiempo estimado de contratación
- Acceso a reportes con todos los KPIs del proceso: tiempo medio de contratación, calidad por fuente, tasa de abandono, embudo por etapa, etc.
- Multilenguaje e identificación automática de zonas horarias para entrevistas
- Una experiencia fluida y moderna en dispositivos desktop y móviles

## Para
aumentar drásticamente la eficiencia operativa del equipo de Recursos Humanos, reducir el tiempo de contratación, y tomar mejores decisiones basadas en datos e IA generativa.

---

## Criterios de Aceptación

### 🔗 Gestión de Ofertas Laborales
- [ ] Crear, editar, publicar y despublicar ofertas
- [ ] Asignar hiring managers y responsables
- [ ] Publicar automáticamente en LinkedIn, Indeed, etc.

### 🧑‍💼 Gestión de Candidatos
- [ ] Importar CVs desde correo, portales externos o carga manual
- [ ] Registro automático o manual de referidos
- [ ] Ver historial, notas, entrevistas y decisiones por cada candidato
- [ ] Avanzar candidatos por etapas de embudo (automático o manual)

### 🧠 IA y Automatización
- [ ] Matching inteligente CV ↔ Oferta
- [ ] Feedback generado post-entrevista
- [ ] Sugerencias de candidatos similares
- [ ] Emails generados automáticamente (convocatorias, rechazos, seguimientos)
- [ ] Reportes con predicciones (tiempo de cierre, probabilidad de éxito)

### 📅 Entrevistas y Pruebas
- [ ] Organización de entrevistas con integración a Zoom/Meet y calendario
- [ ] Registro de evaluaciones
- [ ] Resultados automáticos de pruebas externas

### 💬 Colaboración
- [ ] Comentarios en tiempo real por perfil y posición
- [ ] Menciones @usuario y tareas asignables
- [ ] Historial de actividad

### 📊 KPIs y Reportes
- [ ] Embudo completo por posición
- [ ] Tiempos promedio por etapa y por reclutador
- [ ] Conversión por fuente y canal
- [ ] Análisis de calidad vs velocidad

---

## 🌐 Requisitos Técnicos

### Frontend
- React con Vite
- TailwindCSS + ShadCN para UI moderna
- Soporte multilenguaje (i18n)
- Integración con Google Calendar, Zoom, Slack, LinkedIn
- App responsive y rápida

### Backend
- NestJS + Prisma ORM
- PostgreSQL como base de datos principal
- Integración con IA generativa (OpenAI API) y analítica
- Envío de emails programáticos (SendGrid, Mailgun)
- Soporte para webhooks y APIs externas (LinkedIn, Codility)
- Websockets para colaboración en tiempo real

### Base de Datos (PostgreSQL)
- Normalización 3FN
- Tablas clave: `Users`, `Candidates`, `Jobs`, `Applications`, `Interviews`, `Notes`, `Assessments`, `Tasks`, `AI_Matches`, `Feedback`, `Reports`
- Ver modelo completo en sección aparte

### Integraciones Confirmadas
- Google Calendar / Outlook
- Slack / Email
- Zoom / Meet
- LinkedIn / Indeed
- HackerRank / Codility

---

## 🧩 Casos de Uso Principales

### 1. Publicar una Oferta de Trabajo
**Actor:** Reclutador  
**Flujo principal:**
1. El reclutador accede al panel de creación de oferta.
2. Completa título, descripción, requisitos, localización y tipo de trabajo.
3. Asigna responsables (hiring manager).
4. Define etapas del proceso de selección.
5. Publica la oferta internamente o en portales externos (LinkedIn, Indeed).

---

### 2. Recibir y Registrar Candidatos
**Actor:** Candidato (externo), Reclutador (interno)  
**Flujo principal:**
1. Un candidato se postula vía LinkedIn, correo, formulario web o referido.
2. El sistema ingesta automáticamente el perfil o CV.
3. El reclutador revisa y enriquece el perfil si es necesario.
4. El sistema evalúa el match semántico entre el CV y la oferta.

---

### 3. Revisar Perfil del Candidato
**Actor:** Reclutador, Hiring Manager  
**Flujo principal:**
1. Se accede al perfil completo del candidato.
2. Se visualiza CV, experiencia, comentarios internos, historial de entrevistas y evaluaciones.
3. Se deja feedback o se etiqueta a otro usuario.
4. Se avanza o rechaza el candidato.

---

### 4. Coordinar Entrevista
**Actor:** Reclutador  
**Flujo principal:**
1. El reclutador propone fechas con disponibilidad desde Google/Outlook Calendar.
2. Se selecciona tipo de entrevista (remota, presencial, híbrida).
3. Se asigna entrevistador/es.
4. Se envía la invitación automática por email + calendario.

---

### 5. Evaluar Candidato
**Actor:** Entrevistador  
**Flujo principal:**
1. El entrevistador accede al formulario de evaluación en la plataforma.
2. Completa comentarios, calificaciones y recomendaciones.
3. El sistema genera automáticamente un resumen con IA generativa.

---

### 6. Aplicar Pruebas Técnicas
**Actor:** Reclutador, Candidato  
**Flujo principal:**
1. El reclutador selecciona una prueba de HackerRank/Codility.
2. El sistema envía el link personalizado al candidato.
3. Se registran los resultados automáticamente.

---

### 7. Colaborar en el Proceso de Selección
**Actor:** Hiring Manager, Reclutador  
**Flujo principal:**
1. Se comentan perfiles directamente en su ficha.
2. Se asignan tareas internas (entrevistar, revisar, decidir).
3. Se recibe notificación cuando un usuario es mencionado.

---

### 8. Comunicarse con el Candidato
**Actor:** Reclutador  
**Flujo principal:**
1. Se redacta o se genera automáticamente un correo de seguimiento.
2. Se envía al candidato (convocatoria, rechazo, feedback, etc.).
3. Se registra el historial de comunicaciones.

---

### 9. Generar Reportes y KPIs
**Actor:** Reclutador, Hiring Manager  
**Flujo principal:**
1. Se accede al dashboard de métricas.
2. Se visualiza información sobre embudos, fuentes, duración, éxito por canal.
3. El sistema ofrece insights automáticos y recomendaciones.

---

### 10. Cerrar Proceso de Selección
**Actor:** Reclutador  
**Flujo principal:**
1. Se selecciona un candidato finalista.
2. Se notifica a todos los participantes (internos y externos).
3. Se cierra la oferta y se archivan los datos.

---

## 🎯 Características Diferenciales

1. 🧠 IA Generativa avanzada en feedback y emails automáticos  
2. ⚡️ Interfaz colaborativa en tiempo real (tipo Notion o Google Docs)  
3. 📈 Dashboards predictivos e interactivos  
4. 📂 Origen múltiple de candidatos (LinkedIn, referidos, emails, etc.) sin fricción  
5. 🌎 Zona horaria automática, integración 100% con calendarios  
6. ✨ UX enfocada en contratación rápida y sin pasos innecesarios  
7. 📱 Aplicación responsive de alto rendimiento

---

## ⚠️ Esta historia de usuario contiene toda la información necesaria para derivar fácilmente:

- Modelo de datos completo con entidades, atributos y relaciones
- Implementación frontend y backend
- Casos de uso principales
- Diseño del sistema a alto nivel
- Diagramas C4 de todos los niveles (no incluidos aquí por claridad, pero pueden derivarse directamente)
