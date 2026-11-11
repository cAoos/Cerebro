---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 🗺️ Explorer del Agentforce Builder

El [[🏗️ Agentforce Builder]] tiene **tres secciones**: **Explorer (1)**, **Editor (2)** y **Agentforce Assistant (3)**.

![[builder-tres-paneles.jpg]]

## 1️⃣ Explorer: todo el detalle del agente
Las mismas 5 secciones existen en **todo tipo de agente**:

| | Sección | Qué contiene |
|---|---|---|
| ⚙️ | **Settings** | Agent Details: nombre, rol, descripción, **idioma** y otra configuración |
| 🗂️ | **Subagents** | El **Agent Router** y la lista de [[🗂️ Subagentes\|subagentes]]. Cada subagente es una **carpeta** con su configuración y sus acciones |
| 🔣 | **Variables** | Valores que se guardan y reutilizan en la lógica y el razonamiento, y **controlan cómo decide** el agente |
| 🔌 | **Connections** | Configuración que **une el agente a los canales**: Messaging, Slack, Voice |
| 📚 | **Data** | Fuentes para recuperar conocimiento, por ejemplo un PDF de FAQs subido a Data 360. Ver [[📚 Agentforce Data Library]] |

🧭 **Agent Router**: componente central que **decide qué subagente usar** según lo que escribe el usuario y el **historial de la conversación**. Ver [[🌍 Atlas Reasoning Engine]].

![[builder-explorer-subagentes.jpg|300]]

## 2️⃣ Editor
Cada elemento que abres en el Explorer **abre una pestaña** en el editor. Se ve en **Canvas** (lenguaje natural, atajos, inline actions, selector de recursos) o **Script** (resaltado de sintaxis, **autocompletado** y validación). Ver [[📜 Agent Script]].

## 3️⃣ Agentforce Assistant
Siempre disponible para construir en lenguaje natural: "Crea un subagente llamado Case Management". Puede hacer **preguntas aclaratorias**, **muestra los cambios propuestos** y **pide confirmación** antes de aplicarlos.

> ⚠️ Ojo de examen: **Agent Router** = elige el subagente según input + historial. **Connections** = canales (Messaging, Slack, Voice). **Data** = fuentes de conocimiento. **Variables** = controlan decisiones. El Assistant **nunca aplica cambios sin confirmación**.

## 🔁 Repaso #flashcards
¿Cuáles son las tres secciones del Agentforce Builder?::Explorer, Editor (Canvas/Script) y Agentforce Assistant.
¿Qué secciones tiene el Explorer?::Settings, Subagents, Variables, Connections y Data.
¿Qué hace el Agent Router?::Decide qué subagente usar según el input del usuario y el historial de la conversación.
¿Para qué sirven las Connections de un agente?::Unen el agente a canales como Messaging, Slack o Voice.
¿Para qué sirven las Variables de un agente?::Guardan y reutilizan valores en la lógica y el razonamiento, y controlan cómo decide el agente.
¿Aplica cambios el Agentforce Assistant directamente?::No: muestra los cambios propuestos y pide confirmación.
