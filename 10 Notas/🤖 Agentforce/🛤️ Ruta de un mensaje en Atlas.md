---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 🛤️ Ruta de un mensaje en Atlas

Cómo el [[🌍 Atlas Reasoning Engine]] procesa un mensaje en **5 pasos**:

| Paso | Qué pasa | Tipo |
|------|----------|------|
| 1️⃣ | El usuario escribe una pregunta o solicitud | — |
| 2️⃣ | El agente la envía al **subagente inicial** | — |
| 3️⃣ | Resuelve las **instrucciones de razonamiento** del subagente **en el orden escrito**. Si cambia de subagente, redirige al instante | 🔒 **Determinístico**: expresiones programáticas **antes** del LLM |
| 4️⃣ | Arma el **prompt** para el LLM con: instrucciones del agente · historial reciente · instrucciones resueltas · acciones disponibles del subagente | 🧱 Construcción |
| 5️⃣ | El LLM decide: **responder** al usuario (cierra el ciclo) o **ejecutar una acción** (y la lógica posterior a ella) | 🎲 **LLM** |

```text
🗣️ Mensaje ─► 🗂️ Subagente inicial ─► 🔒 Resolver instrucciones (en orden) ─► 🧱 Prompt ─► 🧠 LLM
                       ▲                                                              │
                       │                                              ┌──── 💬 responder
                       └────── nueva pregunta del usuario ◄───────────┤
                                                                      └──── ⚡ ejecutar acción
```

> ⚠️ Ojo de examen: el paso 3 es **determinístico**: las expresiones se resuelven **antes** de llamar al LLM. Y qué **lleva el prompt** que se le envía al LLM (las 4 piezas del paso 4).

## 🔁 Repaso #flashcards
¿Cuáles son los 5 pasos de un mensaje en Atlas?::1. Entra el mensaje · 2. Va al subagente inicial · 3. Resuelve instrucciones en orden (determinístico) · 4. Arma el prompt · 5. El LLM responde o ejecuta una acción.
¿Qué incluye el prompt que Atlas envía al LLM?::Instrucciones del agente, historial reciente, instrucciones resueltas y acciones disponibles del subagente.
¿Qué parte del proceso es determinística?::La resolución de las instrucciones del subagente, antes de comunicarse con el LLM.
