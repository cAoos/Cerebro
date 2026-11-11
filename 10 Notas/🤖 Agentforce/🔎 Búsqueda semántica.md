---
tipo: nota
tema: trust-layer
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-27
---
# 🔎 Búsqueda semántica

Usa **machine learning y métodos de búsqueda** para encontrar información relevante en **otras fuentes de datos** y la incluye automáticamente en el prompt.

- 🧠 Busca por **significado**, no por palabras exactas (ver [[💭 Análisis semántico del lenguaje]]).
- 📚 Es el "R" de **RAG**: recupera los fragmentos útiles antes de llamar al LLM.
- 📥 Es una de las formas de [[📥 Grounding dinámico]].

## 🧪 Ejemplo
Un cliente pregunta "¿cómo devuelvo unas zapatillas que me quedaron chicas?". La búsqueda semántica encuentra el artículo de Knowledge **"Política de cambios y devoluciones"**, aunque no diga "zapatillas" ni "chicas", y lo agrega al prompt.

> ⚠️ Ojo de examen: si piden responder con **documentos o artículos** (datos no estructurados) y no con campos de un registro → búsqueda semántica / RAG, no merge fields.

## 🔁 Repaso #flashcards
¿Qué hace la búsqueda semántica en la Trust Layer?::Usa machine learning para encontrar información relevante en otras fuentes y la agrega al prompt automáticamente.
¿En qué se diferencia de una búsqueda por palabras clave?::Busca por significado, no por coincidencia exacta de palabras.
