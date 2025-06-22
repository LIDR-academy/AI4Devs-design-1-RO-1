# 🧩 Diagrama C4 – Nivel 3 (Componente: Criba de CV con IA)
## 🎯 Descripción general
Este módulo permite que el sistema analice postulaciones entrantes y entregue, mediante IA, un resumen útil, fortalezas, debilidades y una puntuación de ajuste (“fitScore”) respecto a la vacante. Esto ayuda a priorizar candidatos y acelerar el proceso.

Se activa cuando un **Application** es recibido o actualizado, y puede ser consultado manualmente desde la UI o programado como una automatización del backend.

## 🧩 Subcomponentes del módulo
### 1. CV Preprocessor
* Extrae y normaliza información de documentos PDF o texto (experiencia, educación, skills).
* Usa bibliotecas como pdf-parse, textract o langchain para estructuración.

### 2. Prompt Builder
* Toma los datos del candidato + descripción del trabajo y construye un prompt óptimo.
* Asegura que el formato sea consistente y claro para el modelo de lenguaje.

### 3. OpenAI Connector
* Llama a la API de OpenAI (gpt-4o), enviando el prompt y recibiendo el resultado estructurado.
* Maneja control de errores, latencia y repetición segura.

### 4. Parser & Validator
* Convierte la respuesta de IA en un JSON con estructura fija:
{ summary, strengths, weaknesses, fitScore }.
* Valida que existan los campos y que el fitScore esté entre 0 y 1.

### 5. Storage Layer
* Guarda el resultado en la tabla IAAnalysis, asociada al Application.
* Expone API para su consulta por el frontend.

## 📥 Interfaces
|Subcomponente      | Interfaces expuestas          	        |Formato    |
|-------------------|-------------------------------------------|-----------|
|CV Preprocessor    | extractCV(fileUrl: string): ParsedData	|JSON       |
|Prompt Builder     | buildPrompt(parsedData, jobData): string	|texto      |
|OpenAI Connector   | sendPrompt(prompt: string): RawResponse	|texto      |
|Parser & Validator | parseResponse(text: string): IAAnalysisDTO|JSON       |
|Storage Layer	    | saveAnalysis(applicationId, analysisDTO)	|DB write   |

## 🧪 Tecnologías recomendadas
|Propósito	            | Tecnología sugerida               |
|-----------------------|-----------------------------------|
|Procesamiento texto    | pdf-parse, textract, langchain    |
|Backend	            | Node.js + TypeScript              |
|LLM API	            | OpenAI (GPT-4o)                   |
|Cola de tareas         | BullMQ + Redis                    |
|Persistencia	        | PostgreSQL (IAAnalysis table)     |
|Seguridad	            | Input sanitization + timeouts     |

## 🗺️ Diagrama C4 – Nivel 3 (Componente Interno)
Procedo ahora a generar el diagrama que representa la arquitectura interna de este módulo específico.

![Diagrama de C4 - Nivel 3](img/diagrama-c4-nivel3.png)