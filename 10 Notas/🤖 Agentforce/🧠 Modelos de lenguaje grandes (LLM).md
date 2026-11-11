---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-23
---
# 🧠 Modelos de lenguaje grandes (LLM)

Modelo entrenado con muchísimo texto para **entender y generar lenguaje parecido al humano**. Se apoya en el [[🗣️ Procesamiento de lenguaje natural (NLP)|NLP]] y el aprendizaje automático. Ejemplos: ChatGPT, Gemini, Claude.

- 🔮 **Cómo funciona:** predice **un [[🪙 Tokens|token]] a la vez**: el siguiente, y el siguiente, y el siguiente… hasta completar la respuesta.
- 📚 **No es una biblioteca:** no guarda libros, guarda **patrones** y relaciones entre palabras. No "comprende" como una persona.
- ⚙️ **Parámetros:** lo que el modelo aprende al entrenarse. Son miles de millones: GPT-3 tenía ~175 mil millones, GPT-4 ~1,76 billones. Más parámetros, más capacidad, pero también más cómputo, más impacto ambiental y riesgo de sesgos.

> ⚠️ Un LLM es una **herramienta, no una fuente de verdad**. Por eso en Salesforce se le da contexto con RAG (ver [[🗂️ Datos estructurados, semiestructurados y no estructurados]]).

Cómo se entrena: [[🎓 Entrenamiento frente a ajuste de un LLM]].

> [!note]- 🔢 Versiones
> Cada versión mantiene la arquitectura, pero cambian la escala, los datos y los parámetros: GPT-1 → GPT-2 → GPT-4. Además existen variantes ajustadas (RoBERTa y DistilBERT a partir de BERT) y familias por nivel de capacidad (Claude Haiku, Sonnet, Opus).

## 🔁 Repaso #flashcards
¿Cómo genera texto un LLM?::Prediciendo un token a la vez, el siguiente más probable según los patrones que aprendió.
¿Qué son los parámetros de un LLM?::Los factores que el modelo aprende durante el entrenamiento; determinan su capacidad para captar patrones.
