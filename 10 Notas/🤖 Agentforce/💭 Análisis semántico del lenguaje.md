---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-22
---
# 💭 Análisis semántico del lenguaje

El [[🧩 Análisis sintáctico del lenguaje|análisis sintáctico]] saca la estructura, pero no la parte "humana". El semántico busca **el significado**: cómo se siente la persona, qué quiere y en qué situación lo dice. Hay tres técnicas:

| Técnica | Pregunta que responde | Ejemplo |
|---------|----------------------|---------|
| 😊😠 **Análisis de opiniones** (*sentiment*) | ¿Es positivo, negativo o neutro? | "Tuve que esperar mucho para el corte de pelo" → negativo |
| 🎯 **Análisis de intenciones** (*intent*) | ¿Qué quiere conseguir la persona? | "No puedo iniciar sesión" → quiere recuperar el acceso → se le ofrece restablecer la contraseña |
| 🧭 **Análisis de contexto** (discurso) | ¿Qué significa aquí, según la conversación? | "Tenían una pelota": ¿un baile, un balón o un rato divertido? |

> ⚠️ Ojo de examen: el **análisis de intenciones** es lo que hace un agente de Agentforce cuando **clasifica el mensaje del usuario en un subagent** (antes *topic*) para decidir qué acciones usar.

## 🔁 Repaso #flashcards
¿Cuáles son las tres técnicas de análisis semántico?::Opiniones (sentiment), intenciones (intent) y contexto (discurso).
¿Qué técnica usa un agente para entender qué quiere el usuario?::El análisis de intenciones.
