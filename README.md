# Introducción a la Creación de RAGs (Retrieval-Augmented Generators) con OpenAI

## 📖 Enunciado del Laboratorio
Este laboratorio introduce a los estudiantes en los conceptos fundamentales y la implementación práctica de **Retrieval-Augmented Generators (RAGs)** utilizando las herramientas de **OpenAI** y el framework **LangChain**.  
Al finalizar, los estudiantes habrán adquirido experiencia práctica construyendo y entendiendo RAGs, culminando en la entrega de **dos repositorios en GitHub** que muestran su trabajo.

- **Repositorio 1**: Implementación básica del tutorial de LangChain LLM Chain.  
- **Repositorio 2**: Proyecto RAG utilizando Pinecone como base de datos vectorial y OpenAI para embeddings y LLM.

---

## 🎯 Objetivos
- Comprender el concepto de **Retrieval-Augmented Generation (RAG)**.  
- Aprender cómo LangChain integra mecanismos de recuperación con modelos generativos.  
- Construir un pipeline RAG con Pinecone y OpenAI.  
- Entregar dos repositorios en GitHub con código y documentación.

---

## 🛠️ Preparación Previa
Antes de comenzar, revisa los siguientes tutoriales oficiales de LangChain:
- [Tutorial LLM Chain](https://python.langchain.com/docs/tutorials/llm_chain/)  
- [Tutorial RAG](https://python.langchain.com/docs/tutorials/rag/)  

Estos recursos proporcionan la base necesaria para construir aplicaciones avanzadas con LangChain.

---

## 📂 Arquitectura del Proyecto

### Repositorio 1: LLM Chain Básico
- **Componentes**:
  - Modelo `ChatOpenAI` desde `langchain_openai`.
  - Plantillas de prompt simples.
  - Ejecución de cadenas con consultas de usuario.
- **Objetivo**: Demostrar cómo conectar un LLM con un prompt y ejecutar consultas.

### Repositorio 2: Proyecto RAG
- **Componentes**:
  - **Document Loader**: Carga de archivos de texto o PDF.  
  - **Text Splitter**: División de documentos en fragmentos para embeddings.  
  - **Embeddings**: Uso de embeddings de OpenAI (`text-embedding-3-small` o similar).  
  - **Vector Store**: Pinecone como base de datos vectorial.  
  - **Retriever**: Consulta a Pinecone para obtener fragmentos relevantes.  
  - **Agente/Chain**: Combina el contexto recuperado con el LLM para responder preguntas.

---

## ⚙️ Instalación

Clona el repositorio y instala las dependencias:

```bash
git clone <repo-url>
cd <repo-folder>
pip install -U langchain langchain-community langchain-openai pinecone
```

Configura tus claves de API como variables de entorno:

```bash
export OPENAI_API_KEY="tu_api_key_de_openai"
export PINECONE_API_KEY="tu_api_key_de_pinecone"
```

---

## ▶️ Ejecución del Código

### Repositorio 1 (LLM Chain)
```bash
python llm_chain_demo.py
```

### Repositorio 2 (RAG Project)
```bash
python rag_pipeline.py
```

---

## 📸 Ejemplo de Salida

- **LLM Chain**:  
  Entrada: `"Explica qué es la descomposición de tareas"`  
  Salida: `"La descomposición de tareas es el proceso de dividir tareas complejas en subtareas manejables..."`

- **RAG Project**:  
  Entrada: `"¿Cuál es el método estándar para la descomposición de tareas?"`  
  Salida:  
  El modelo recupera contexto relevante desde Pinecone y genera una respuesta enriquecida.

---

## 📝 Requisitos del README
- Arquitectura y componentes explicados.  
- Instrucciones paso a paso de instalación y ejecución.  
- Ejemplos de salida incluidos.  

---

## ⚠️ Nota Importante
Durante el taller enfrentamos **problemas de compatibilidad con librerías y el entorno en Jupyter**:
- Diferencias entre versiones de `pinecone-client` y `pinecone` que generaban errores de conexión.  
- Algunos imports de LangChain (`create_openai_functions_agent`) fueron deprecados en versiones recientes.  
- Inconsistencias del kernel de Jupyter dificultaron mantener un entorno estable.  

👉 Por estas razones, **no pudimos ejecutar el pipeline RAG de forma completa dentro de Jupyter**, aunque el código y la documentación siguen las mejores prácticas y los tutoriales oficiales. Los repositorios sirven como referencia y artefacto de aprendizaje.

---

## ✅ Criterios de Evaluación
- Código completo y alineado con los tutoriales.  
- Documentación clara y detallada en el README.  
- Organización adecuada de los repositorios en GitHub.  

