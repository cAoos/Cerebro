---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 🎧 Agentforce Service Agent

Agentforce for Service es un **agente de IA conversacional y autónomo para atención al cliente**. A diferencia de los chatbots tradicionales con diálogos rígidos, usa **IA generativa** para trabajar **24/7** en portales de autoservicio y canales de mensajería. Resuelve tareas, toma decisiones y responde de forma natural con la voz de la marca.

Está **anclado en datos de negocio y en la base de conocimiento**, así que responde con contexto. Libera al equipo de servicio para trabajo de más valor.

## 🌟 Beneficios clave
| | Beneficio | Qué significa |
|---|---|---|
| 🕐 | **Responde 24/7** | Contesta, **desvía casos** (case deflection) y cumple metas de servicio a cualquier hora |
| 💬 | **Responde natural** | IA generativa con contexto y la voz de la marca |
| ❓ | **Aclara** | Las instrucciones le dicen qué preguntas hacer para obtener información precisa |
| 🙋 | **Pasa a humanos** | Transfiere o **escala** a un agente humano los casos complejos |
| 🚀 | **Se despliega rápido** | Plantillas de servicio y flujos existentes: **sin escribir diálogos, definir intents, mantener árboles de conversación ni entrenar LLMs** |
| 🛡️ | **Datos confiables** | Grounding en artículos de Knowledge, casos similares y datos del CRM. Todas las llamadas al LLM pasan por el [[🛡️ Einstein Trust Layer]] |

## ⚙️ Qué lo mueve
Tres piezas que trabajan juntas: **[[🗂️ Subagentes|subagentes]]**, **[[⚡ Acciones de agente|acciones]]** e **instrucciones**. Primero se crea el subagente y dentro de él van las acciones y las instrucciones; **ambas deben estar ligadas a un subagente**. Ejemplos en [[🧰 Casos de uso de Service Agent]].

Su conocimiento viene del [[📚 Agentforce Data Library]].

## 🛠️ Cómo se crea
Setup → Quick Find → **New Agent** → elegir el tipo de agente.

Ver también: [[🆚 Agentforce Service Agent frente a Einstein Bots]] · [[🧑‍🤝‍🧑 Tipos de agentes de Agentforce]]

> ⚠️ Ojo de examen: Service Agent **no requiere entrenar modelos, definir intents ni diseñar diálogos**: eso era Einstein Bots. Se arranca con **subagentes y acciones prediseñados** y se mejora iterando **instrucciones en lenguaje natural**. Escalar a humano es una capacidad estándar.

> 🪄 Para el **agente humano** de servicio (no el cliente) está [[🪄 Agentforce Service Assistant]]: resumen y plan paso a paso en el Case.

## 🔁 Repaso #flashcards
¿Qué es Agentforce Service Agent?::Un agente de IA autónomo y conversacional que atiende clientes 24/7 en portales y canales de mensajería, con IA generativa y anclado en datos del negocio y Knowledge.
¿Qué tres elementos definen cómo actúa Service Agent?::Subagentes, acciones e instrucciones. Acciones e instrucciones siempre van ligadas a un subagente.
¿Qué NO necesitas hacer para desplegar Service Agent?::Escribir diálogos, definir intents, mantener árboles de conversación ni entrenar LLMs.
¿En qué fuentes se ancla Service Agent?::Artículos de Knowledge, casos similares y datos del CRM, todo pasando por el Einstein Trust Layer.
¿Cómo se crea un agente nuevo desde Setup?::Quick Find → New Agent → elegir el tipo de agente.
