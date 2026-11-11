---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-22
---
# 🧩 Análisis sintáctico del lenguaje

Desarma el texto en piezas para encontrar su **estructura gramatical**. Es la primera mitad del análisis que hace [[🔀 NLU frente a NLG|NLU]]. La otra mitad, el significado, es el [[💭 Análisis semántico del lenguaje]].

| Técnica | Qué hace |
|---------|----------|
| ✂️ **Segmentación** | Divide un texto largo en oraciones, guiándose por la puntuación |
| 🪙 **Tokenización** | Divide las oraciones en [[🪙 Tokens]] |
| 🌱 **Derivación** (*stemming*) | Corta la palabra a su raíz sin mirar el contexto: *breaking, breaks, unbreakable* → *break* |
| 📖 **Lematización** | Llega a la raíz **teniendo en cuenta qué parte del discurso es**, así que acierta más |
| 🏷️ **Etiquetado de partes del discurso** | Marca cada palabra como sustantivo, verbo, adjetivo… |
| 🔎 **NER** (reconocimiento de entidades nombradas) | Encuentra personas, fechas, lugares y organizaciones en el texto |

## 🧪 Ejemplo: derivación frente a lematización
| Frase | 🌱 Derivación | 📖 Lematización |
|-------|---------------|-----------------|
| "I'm going outside to rake **leaves**" | *leave* ❌ | *leaf* ✅ |
| "He always **leaves** the key in the lock" | *leave* ✅ | *leave* ✅ |

> [!note]- 📚 Elementos del lenguaje natural
> Vocabulario · gramática · sintaxis · semántica · **pragmática** (contexto e intención según la cultura o la región) · discurso y diálogo · fonética y fonología · morfología (cómo se forman las palabras)

## 🔁 Repaso #flashcards
¿En qué se diferencia la lematización de la derivación?::La lematización tiene en cuenta la parte del discurso, así que llega a una raíz válida (leaves → leaf); la derivación solo corta la palabra.
¿Qué hace NER?::Identifica y clasifica entidades nombradas: personas, fechas, lugares, organizaciones.
