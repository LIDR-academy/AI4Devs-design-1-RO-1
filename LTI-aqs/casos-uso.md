# ✅ Caso de Uso 1: Crear y gestionar una vacante (con IA)
**Nombre**: Crear Vacante con Sugerencias de IA
**Actor principal**: Reclutador
**Actores secundarios**: Manager de contratación
**Precondiciones**: El usuario está autenticado y tiene rol autorizado para crear vacantes.
**Postcondición**: La vacante queda publicada internamente (o externamente, si se desea).

# Flujo principal:
1. El reclutador accede al panel de creación de vacantes.
2. Completa los campos básicos (título, descripción, requisitos).
3. Activa el botón “Sugerencias IA”.
4. El sistema genera recomendaciones de:
* Habilidades clave a incluir.
* Preguntas de screening.
* Formato de descripción optimizado.
5. El reclutador revisa y edita el contenido sugerido.
6. Selecciona el canal de publicación (interno / externo).
7. El manager revisa la vacante y la aprueba.
8. El sistema publica la vacante y queda activa para postulaciones.

# Flujos alternativos:
* Si el manager no aprueba, la vacante queda en estado “borrador”.
* Si falla la llamada a la IA, se muestra mensaje y continúa flujo manual.

# ✅ Caso de Uso 2: Evaluar postulaciones en colaboración
**Nombre: Revisión Colaborativa de Candidatos**
**Actor principal:** Reclutador
**Actores secundarios:** Manager de contratación, IA del sistema
**Precondiciones:** Hay una o más postulaciones asociadas a una vacante activa.
**Postcondición:** Candidatos quedan clasificados para avanzar, rechazar o entrevistar.

# Flujo principal:
1. El reclutador entra a la lista de postulaciones de una vacante.
2. Visualiza una tabla con datos clave (nombre, experiencia, educación, etc.).
3. Activa “Resumen IA” para ver el análisis automático de cada CV:
* Fortalezas destacadas.
* Red flags detectadas.
* Recomendación preliminar (fit alto / medio / bajo).
4. El manager agrega comentarios y etiquetas (👍, 👎, ⚠️).
5. El equipo decide en conjunto qué candidatos avanzan.
6. El sistema actualiza el estado de cada postulación.

# Flujos alternativos:
* Si hay desacuerdo, se deja comentario y se deja pendiente la decisión.

# ✅ Caso de Uso 3: Selección final y cierre del proceso
**Nombre:** Selección de Candidato Final
**Actor principal:** Manager de contratación
**Actores secundarios:** Reclutador
**Precondiciones:** El proceso de entrevistas ha concluido y hay feedback registrado.
**Postcondición:** Se marca un candidato como “Contratado” y se cierra la vacante.

# Flujo principal:
1. El manager accede a la etapa final de la vacante.
2. Consulta el historial de cada candidato finalista:
* CV original
* Notas de entrevistas
* Evaluaciones del equipo
3. Utiliza IA para ver comparación automática entre finalistas.
4. Selecciona un candidato y lo marca como “Contratado”.
5. El sistema actualiza el estado de la vacante a “Cerrada”.
6. Genera reporte resumen exportable (Excel o PDF).
7. El resto de los candidatos quedan marcados como “No seleccionados”.

# Flujos alternativos:
* Si ningún candidato es adecuado, se reactiva la vacante y se reinicia el proceso.

# 📊 Diagrama de Casos de Uso UML
Este es un esquema textual del diagrama.
```
            +-----------------+
            |   Reclutador    |
            +-----------------+
                   |
    +---------------------------------------+
    |  Crear vacante con IA                 |
    +---------------------------------------+
                   |
    +---------------------------------------+
    |  Ver y gestionar postulaciones        |
    +---------------------------------------+
                   |
    +---------------------------------------+
    |  Generar feedback y etiquetar         |
    +---------------------------------------+

            +---------------------+
            |   Manager Contrato  |
            +---------------------+
                   |
    +---------------------------------------+
    |  Revisar y aprobar vacante            |
    +---------------------------------------+
                   |
    +---------------------------------------+
    |  Seleccionar candidato final          |
    +---------------------------------------+
 
            +---------------+
            |     IA LTI    |
            +---------------+
                 |     |     |
                Sugerencias, análisis, comparaciones
```