---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-27
---
# 🌍 Atlas Reasoning Engine

Es el **"cerebro" de Agentforce**, la capa agéntica de la plataforma Salesforce. Es un [[⚙️ Reasoning engine]] propietario, diseñado para **simular cómo piensan y planean las personas**. Usa varias técnicas, entre ellas **RAG avanzado**, para analizar la información y decidir las mejores acciones para tareas simples o complejas.

No solo sigue instrucciones: **piensa proactivamente** cuál es la mejor forma de convertirlas en objetivos alcanzables.

- 🎼 Es como un **director de orquesta**: coordina cómo subagentes y acciones atienden la solicitud.
- 🕸️ Está **basado en grafos**: como un diagrama de flujo con **nodos, variables y transiciones**, para seguir rutas predecibles.
- 🔀 A diferencia de los motores basados solo en prompts, **separa el flujo de trabajo de las habilidades conversacionales** usando [[📜 Agent Script]]: **razonamiento híbrido** (predictibilidad de la empresa + flexibilidad del LLM).
- 🛤️ Paso a paso: [[🛤️ Ruta de un mensaje en Atlas]].

## ⚙️ Cómo funciona

| | Concepto | Qué hace |
|---|----------|----------|
| 🔄 | **Reason–act–observe loop (ReAct)** | Piensa un paso, usa una action, revisa el resultado y repite hasta cumplir el objetivo. Si hace falta, **pide aclaraciones** a mitad de la tarea |
| 🗂️ | **Subagent classification** | Asigna cada pedido a un [[🗂️ Subagentes|subagent]]: la "descripción de cargo" de la IA en ese momento. Define **qué actions son válidas y qué políticas aplican** |
| 💬 | **Richer conversations** | Responde en lenguaje natural, maneja preguntas de seguimiento y usa el contexto de la conversación |
| 🔍 | **Visible reasoning** | Muestra sus "pensamientos" (por qué actuó así) para que el admin revise decisiones y evite errores. Se ven en **Agentforce Builder** |

```text
🗣️ Pedido ─► 🗂️ Subagent ─► 🧠 Razonar ─► ⚡ Action ─► 👀 Observar ─┐
                                ▲                                 │
                                └──── ¿falta algo? ◄──────────────┘
                                              │ listo
                                              ▼
                                         📩 Respuesta
```

## ✨ Qué lo diferencia

- ⏰ **Acciones proactivas:** no espera al usuario. Se dispara cuando **cambian datos del CRM**, llega un correo o se acerca una reunión.
- 📥 **Recuperación dinámica de información:** trae datos estructurados y no estructurados de **Data 360**, búsquedas web o documentos internos (ver [[📥 Grounding dinámico]]).
- 🧑‍💼 **Traspaso fluido a un humano:** ante una pregunta difícil o una regla de negocio estricta, pasa la conversación a una persona sin cortar la experiencia.

> 💡 Atlas está **orientado a objetivos**: no solo responde, empuja hacia el resultado aunque el camino no sea lineal (seguimientos, aclaraciones, excepciones).

> ⚠️ Ojo de examen: **topics ahora se llaman subagents** en el nuevo Agentforce Builder. Si el examen dice *topic*, es lo mismo: el trabajo al que Atlas asigna el pedido, con sus actions e instrucciones.

> ⚠️ Ojo de examen: "¿dónde revisa el admin **por qué** el agente eligió una acción?" → el **razonamiento visible** en Agentforce Builder.

Es la versión de Agentforce de la estrategia **ReAct** (ver [[♟️ Estrategias de razonamiento de un LLM]]) y aplica los [[🚧 Guardrails para agentes autónomos]].

## 🔁 Repaso #flashcards
¿Qué es el Atlas Reasoning Engine?::El "cerebro" de Agentforce: un reasoning engine que analiza la información (con RAG) y decide las mejores acciones para cumplir el objetivo.
¿Cuál es el ciclo de Atlas?::Reason–act–observe (ReAct): razona un paso, ejecuta una action, revisa el resultado y repite hasta cumplir el objetivo.
¿Qué es la subagent classification?::Asignar cada pedido a un subagent (antes topic), que define qué actions son válidas y qué políticas aplican.
¿Dónde se ve el razonamiento de Atlas?::En Agentforce Builder (visible reasoning).
¿Qué tres cosas diferencian a Atlas?::Acciones proactivas, recuperación dinámica de información y traspaso fluido a un humano.
