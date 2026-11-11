---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-01
---
# 🧬 Diseñar un subagente

El [[🗂️ Subagentes|subagente]] define el **objetivo** del agente y le da contexto y dirección.

## 🛤️ Cómo se usa en la conversación
1. La conversación entra al **subagente inicial**: por defecto el **Agent Router**, que elige subagente según el **historial reciente** y los subagentes disponibles.
2. El agente **resuelve las instrucciones del subagente en el orden escrito**.
3. Con el resultado **arma un prompt** y lo envía al **LLM**, que razona y actúa.

Ver [[🛤️ Ruta de un mensaje en Atlas]].

## ✏️ Las tres partes
| Parte | Cómo escribirla |
|---|---|
| 🏷️ **Name** | Refleja el **job to be done** (ej: Reservation Management). Con varios subagentes, **nombres no parecidos** o el motor no los distingue |
| 📄 **Description** | **1-3 oraciones**: qué hace y **qué mensajes del usuario deben dispararlo**. **Name + description** + instrucciones del Router deciden el **enrutamiento** |
| 📝 **Instructions** | Mezcla de **lógica programática** ([[📜 Agent Script]]: ruta definida y predecible) y **prompts en lenguaje natural** (conversación flexible) |

![[planear-agente-subagente-reservas.jpg]]

- 💬 Lenguaje natural: "Confirma siempre los detalles de una modificación antes de finalizar".
- 🔒 Programático: la regla de reembolso "solo si canceló hasta 2 días antes del check-in" se escribe como **expresión**, para que el LLM no la malinterprete. Ver [[🎯 Determinismo en Agentforce]].

💡 **Escribe las instrucciones al final**: no puedes escribirlas bien sin saber cuánta lógica pusiste en las acciones y cuánto decide el agente solo.

Al ampliar el alcance (V2), **actualizar la descripción** con los nuevos trabajos.

> ⚠️ Ojo de examen: el enrutamiento usa **nombre + descripción** del subagente. Nombres **parecidos** confunden al motor. Las reglas que **no pueden fallar** van como **lógica programática**, no como prompt. Las instrucciones se escriben **al final**.

## 🔁 Repaso #flashcards
¿Qué subagente recibe por defecto la conversación?::El Agent Router, que elige el subagente según el historial reciente y los subagentes disponibles.
¿Qué usa el agente para decidir qué subagente aplicar?::El nombre y la descripción de cada subagente, comparados con la petición, el historial y las instrucciones del Agent Router.
¿Qué debe decir la descripción de un subagente?::En 1-3 oraciones, qué hace y qué tipo de mensajes del usuario deben dispararlo.
¿Por qué evitar nombres de subagentes parecidos?::Porque el motor de razonamiento no podrá distinguirlos.
¿Cuándo usar lógica programática en vez de lenguaje natural en las instrucciones?::Cuando una regla no puede malinterpretarse, como una condición de reembolso.
¿Por qué escribir las instrucciones del subagente al final?::Porque dependen de cuánta lógica quedó en las acciones y cuánto decide el agente solo.
