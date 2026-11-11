---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 🎭 Diseño del comportamiento de un agente

**Comportamiento de un agente** = los patrones de respuestas y acciones que produce según:
1. 🧑‍💼 su **rol** definido
2. 🎯 sus **objetivos y guardrails**
3. 📝 las **instrucciones** que recibe
4. 🗄️ los **datos** a los que accede
5. 💬 el **input del usuario**

**Diseñar el comportamiento** es definir esas condiciones a propósito para que el agente responda de forma **predecible, segura y alineada con lo que espera el usuario**. Antes el diseñador controlaba la salida; ahora **controla las condiciones** con las que el agente genera su propia salida. El **diseño conversacional (CxD)** y el diseño de comportamiento **van juntos**.

💡 Es como **hacer onboarding a un empleado digital**: no basta un guion; necesita **misión, conocimiento de la empresa y límites claros**.

## 🕰️ Tres eras de la automatización
![[comportamiento-agente-evolucion.jpg]]

| Era | Cómo funciona | Qué se diseña |
|---|---|---|
| 📞 **Pasado: guion (rule-based)** | Árbol telefónico o chatbot básico, **determinista**. Fuera del guion = callejón sin salida | Mapear cada giro del flujo |
| 🧭 **Presente: IA + humanos (asistiva)** | **Copilot**: resume, redacta, sugiere. **El humano es el piloto**; la IA ejecuta cuando le dicen pasos y herramientas | Asistencia en lenguaje natural |
| 🎯 **Futuro: agentes autónomos (por objetivos)** | Eligen acciones y herramientas según **objetivo y contexto**, sin instrucciones paso a paso. Ej: "Resuelve esta disputa de cobro" | **El comportamiento**, no pantallas ni rutas |

Ver [[🦾 Agentes autónomos]].

## 🧠 Principios del mindset agéntico
Diseñar para la **adaptación**, no para la **perfección**:
- 🎯 **Primero la intención**: no un flujo para "perdí mi tarjeta", sino la intención **Seguridad y gestión de activos**; el agente maneja las variaciones del lenguaje.
- 🔍 **Comportamiento predecible y explicable**: si niega un reembolso, **explica por qué y ofrece el siguiente paso**.
- 🧩 **Optimizar el razonamiento, no solo la respuesta**: "¿Dónde está mi pedido?" cambia según el estado (enviado → tracking; entregado → prueba de entrega; retrasado → disculpa y pasos).

**El razonamiento depende del contexto, y el contexto de los datos.** Datos listos para IA: **unificados**, formato consistente, duplicados resueltos con **identity resolution**, seguridad y gobierno, probados, con **revisión humana**. Un agente **no razona más allá de la calidad de sus datos y herramientas**.

Ver también [[🪢 Contrato de cuatro vías]] y [[💥 Fallas de sistema frente a fallas de intención]].

> ⚠️ Ojo de examen: los 5 insumos del comportamiento son **rol, objetivos/guardrails, instrucciones, datos e input del usuario**. En la era asistiva **el humano pilota**; en la autónoma el agente **elige herramientas según el objetivo**. Diseñar desde la **intención**, no desde frases.

## 🔁 Repaso #flashcards
¿Qué define el comportamiento de un agente?::Su rol, sus objetivos y guardrails, las instrucciones, los datos a los que accede y el input del usuario.
¿Qué es diseñar el comportamiento de un agente?::Definir a propósito esas condiciones para que responda de forma predecible, segura y alineada con lo que espera el usuario.
¿Cuáles son las tres eras de la automatización conversacional?::Guion (rule-based), IA + humanos (asistiva, copilot) y agentes autónomos (por objetivos).
¿Quién es el piloto en la era asistiva?::El humano; la IA es el navegante que ejecuta cuando le dan los pasos y herramientas.
¿Qué significa diseñar desde la intención?::Diseñar para el objetivo de alto nivel del usuario, no un flujo por cada frase, para que el agente maneje las variaciones del lenguaje.
¿Qué debe hacer un agente al negar algo, como un reembolso?::Explicar por qué y ofrecer el siguiente paso o alternativa.
