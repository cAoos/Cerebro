---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🛠️ ADLC Skills

Son **skills open source** que dejan a los **coding agents** (Claude Code, Cursor…) **construir, probar y observar agentes de Agentforce** desde cualquier IDE, **sin cambiar de herramienta**.

## 3️⃣ Las tres skills base
| | Skill | Qué hace |
|---|-------|----------|
| 🏗️ | **Develop** | Construir agentes de Agentforce desde cualquier IDE |
| 🧪 | **Test** | Validar el comportamiento del agente sin salir de tus herramientas |
| 👀 | **Observe** | Monitorear y optimizar su desempeño |

Siguen el [[🔁 Ciclo de vida de un agente (ADLC)]].

## 🔪 ¿Y qué es un skill de un agente?
Las **tareas específicas** que un agente sabe hacer: buscar pedidos, procesar reembolsos, enviar correos, sacar reportes. Como una **navaja multiusos**: cada herramienta hace una cosa bien, y el agente **elige la adecuada** para el trabajo.

## 🤖 Cómo encaja Claude Code
- 🔌 Se conecta nativo por [[🔌 MCP en Salesforce|MCP servers]] + ADLC Skills.
- 🏠 Construye, prueba y observa agentes **sin iniciar sesión en Salesforce**.
- 🔒 **Hereda la confianza empresarial**: todo pasa por la Trust Layer, con FLS y sharing.
- 🤝 No hay que elegir entre "mi propio agente" y Agentforce: con **Agentforce Labs** y las skills se tiene seguridad y ciclo de vida completo.
- 🔀 Es **agnóstico de modelo**: por el **LLM Gateway** se conecta a Claude, Gemini o GPT sin *lock-in* (ver [[🔌 Opciones de LLM en Salesforce]]). **Agentforce Vibes 2.0** usa **Claude Sonnet 4.5** por defecto.

> 💡 **Agentforce Labs** ([labs.agentforce.com](https://labs.agentforce.com/)): entorno experimental en vivo, sin configuración ni espera, para probar agentes headless.

> ⚠️ Ojo de examen: hay **+30 ADLC Skills** preconfiguradas y **+60 herramientas MCP**. Las 3 base: **Develop · Test · Observe**.

> 🎒 Qué archivos tiene una skill (SKILL.md, references, scripts, evals) y el repo **sf-skills**: [[🎒 Anatomía de una skill]].

## 🔁 Repaso #flashcards
¿Qué son las ADLC Skills?::Skills open source para que coding agents como Claude Code o Cursor construyan, prueben y observen agentes de Agentforce desde cualquier IDE.
¿Cuáles son las 3 ADLC Skills base?::Develop, Test y Observe.
¿Qué es un skill de un agente?::Una tarea específica que el agente sabe hacer (buscar pedidos, reembolsos, correos); el agente elige la adecuada para cada trabajo.
¿Qué es Agentforce Labs?::Un entorno experimental en vivo, sin configuración, para empezar a construir agentes headless.
