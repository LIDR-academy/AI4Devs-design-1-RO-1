# Prompts.md - Documentación del Proceso de Diseño LTI

## Conversación de Diseño del Sistema ATS

### Prompt Inicial del Usuario

```
Con la siguiente información:

Tú misión será diseñar y documentar un sistema de software siguiendo las fases de investigación y análisis, casos de uso, modelado de datos, y diseño de alto nivel.
¿Y qué sistema? El de LTI.
LTI es una startup que quiere desarrollar el ATS (Applicant-Tracking System) del futuro.
Todavía no hay nada creado, así que toca ponerse el gorro de product manager y definir esas funcionalidades clave que harán brillar a LTI por encima de los competidores: aumentar la eficiencia para los departamentos de HR, mejorar la colaboración en tiempo real entre reclutadores y managers, automatizaciones, asistencia de IA en diversas tareas...es el momento de hacer brainstorming, investigar cuáles pueden ser las claves del éxito, y dejarlo plasmado para el resto del equipo.
Tu misión es diseñar la primera versión del sistema, entregando los siguientes artefactos:
Descripción breve del software LTI, valor añadido y ventajas competitivas. Explicación de las funciones principales. Añadir un diagrama Lean Canvas para entender el modelo de negocio
Descripción de los 3 casos de uso principales, con el diagrama asociado a cada uno
Modelo de datos que cubra entidades, atributos (nombre y tipo) y relaciones
Diseño del sistema a alto nivel, tanto explicado como diagrama adjunto
Diagrama C4 que llegue en profundidad a uno de los componentes del sistema

Documenta todo en un único documento markdown (.md) con el nombre LTI-DCGC, y exporta el chat en un archivo llamado prompts.md,

Antes de comenzar, realiza las preguntas que creas pertinentes
```

### Respuesta de Claude - Preguntas Estratégicas

Claude hizo las siguientes preguntas clave para entender mejor el contexto:

#### Preguntas sobre el contexto del negocio:
1. **Mercado objetivo**: ¿En qué tipo de empresas se enfoca LTI? (startups, PYMES, grandes corporaciones, o un mix?)
2. **Geografía**: ¿Es un producto para el mercado latinoamericano, global, o específicamente para algún país?
3. **Competidores principales**: ¿Conoces los ATS que consideran como competencia directa? (ej: Workday, BambooHR, Greenhouse, etc.)

#### Preguntas técnicas:
4. **Presupuesto y equipo**: ¿Hay restricciones de presupuesto o tamaño de equipo de desarrollo que deba considerar?
5. **Tecnologías preferidas**: ¿Existe alguna preferencia o restricción tecnológica? (cloud provider, lenguajes, etc.)
6. **Integraciones clave**: ¿Qué integraciones consideras esenciales desde el MVP? (LinkedIn, job boards, HRIS, calendarios, etc.)

#### Preguntas sobre funcionalidades:
7. **IA específica**: ¿Qué capacidades de IA tienen más prioridad? (screening automático, matching candidatos, generación de reportes, chatbots, etc.)
8. **Usuarios principales**: Además de HR y managers, ¿hay otros roles importantes? (candidatos, agencias de reclutamiento, etc.)
9. **Compliance**: ¿Hay regulaciones específicas que deba considerar? (GDPR, normativas locales de privacidad, etc.)
10. **Modelo de pricing**: ¿Tienen ya una idea del modelo de negocio? (SaaS por usuario, por empresa, freemium, etc.)

### Respuesta del Usuario

```
1. Para un proyecto inicial cual recomiendas que sea el mejor mercado objetivo?
2. Se quiere que sea global, que implicaria esto?
3. No los conozco
4. Por ahora al ser la etapa inicial, deberia ser un MVP que se enfoque en resultados, asi que procede pensando en que se tengan restricciones tanto en presupuesto como en equipo
5. Las que recomiendes, que sean asequibles para un proyecto en etapas iniciales
6. Tambien las que recomiendes y creas que son las mejores
7. Todas
8. plantea todos los escenarios posibles, aunque solo se utilicen inicialmente los descritos y solicitados
9. Aplica como si se debieran tener en cuenta
10. No
```

### Investigación de Mercado Realizada

Claude realizó investigación sobre:

1. **Análisis del mercado ATS actual**
   - Tamaño del mercado: $16.04B en 2024, proyectado a $30.51B para 2032
   - CAGR de 8.5% durante el período de pronóstico
   - Norteamérica domina con 92.4% del mercado

2. **Competidores principales identificados**
   - Workday, BambooHR, Greenhouse, iCIMS, Oracle Taleo
   - SAP SuccessFactors, Bullhorn, Jobvite, ADP, Cornerstone OnDemand

3. **Tendencias del mercado**
   - 73% de organizaciones invirtiendo en automatización para 2025
   - Crecimiento del trabajo remoto impulsando adopción
   - IA y ML transformando el landscape del reclutamiento

4. **Stack tecnológico recomendado**
   - Frontend: Next.js 15 + TypeScript + Tailwind CSS
   - Backend: Node.js + NestJS + TypeScript
   - Base de datos: PostgreSQL
   - Cloud: Vercel/Railway + AWS/GCP
   - IA: OpenAI API + Langchain

### Recomendaciones Estratégicas Finales

Claude proporcionó recomendaciones detalladas para:

1. **Mercado objetivo inicial**: PYMES en crecimiento (50-500 empleados)
2. **Estrategia global**: Expansión en 3 fases (LATAM → Norteamérica → Europa/Asia)
3. **Ventajas competitivas**: IA nativa, precios 60% más bajos, UX superior
4. **Modelo de negocio**: Freemium + seat-based SaaS
5. **Roadmap de desarrollo**: MVP en 4-6 meses, features avanzadas en 12 meses

### Confirmación del Usuario

```
me parecen adecuadas, procede con el diseño del sistema, y no olvides agregar todas estas recomendaciones estrategicas en el documento final.
```

### Deliverables Creados

1. **LTI-DCGC.md**: Documento técnico completo con:
   - Recomendaciones estratégicas
   - Descripción del software y valor añadido
   - Lean Canvas del modelo de negocio
   - 3 casos de uso principales con diagramas
   - Modelo de datos detallado
   - Diseño del sistema a alto nivel
   - Diagrama C4 del componente de IA

2. **prompts.md**: Este archivo documentando el proceso

### Metodología Utilizada

1. **Investigación de mercado**: Búsqueda web para entender competidores y tendencias
2. **Análisis estratégico**: Identificación de oportunidades y diferenciadores
3. **Diseño técnico**: Arquitectura escalable y moderna
4. **Validación**: Métricas y KPIs para medir éxito
5. **Documentación**: Artefactos completos para desarrollo

### Insights Clave del Proceso

- **Market Opportunity**: Mercado ATS en crecimiento con $30.5B proyectado para 2032
- **Technology Gap**: Soluciones actuales son complejas y costosas para PYMES
- **AI Advantage**: IA nativa como diferenciador principal vs competidores
- **Global Strategy**: Enfoque regional inicial con expansión gradual
- **Technical Excellence**: Arquitectura moderna preparada para escala

### Próximos Pasos Recomendados

1. **Validación con early adopters** (3 meses)
2. **Fundraising Series A** ($4-6M)
3. **Team building** (12 personas iniciales)
4. **Desarrollo MVP** siguiendo roadmap definido
5. **Go-to-market** en mercado LATAM

---

*Este archivo documenta el proceso completo de diseño del sistema ATS de LTI, desde la investigación inicial hasta las recomendaciones finales de implementación.*