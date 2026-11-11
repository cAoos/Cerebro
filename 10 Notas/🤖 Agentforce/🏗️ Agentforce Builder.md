---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 🏗️ Agentforce Builder

El lugar para **crear, personalizar y probar** agentes predecibles y con conciencia del contexto. El **nuevo Builder** se rediseñó desde cero frente al **legacy builder** (no-code / low-code) para crear agentes **más predecibles y fiables**.

## ✨ Qué trae el nuevo Builder
| | Novedad | Qué significa |
|---|---------|---------------|
| 🔒 | **More determinism** | [[🌍 Atlas Reasoning Engine\|Atlas]] mejorado y **basado en grafos**: antes **todo** lo interpretaba el LLM; ahora el agente puede seguir una ruta definida |
| 📜 | **Programmatic control** | [[📜 Agent Script]]: vista **Canvas** (lenguaje natural) o **Script** (sintaxis resaltada y validación en tiempo real) |
| 🤖 | **Built-in assistance** | Le dices a Agentforce qué quieres y **lo convierte en Agent Script** por ti |
| 🗂️ | **Improved UI** | Explorer **basado en archivos**: más plano, más fácil copiar, pegar y reutilizar la metadata |
| 🔍 | **Powerful previews** | Trazas y depuración detalladas de cada conversación de prueba |

## 🧭 Cómo llegar y crear un agente
![[agentforce-studio-agents.jpg]]

🔲 **App Launcher** → [[🎛️ Agentforce Studio]] → **Agents** → **New Agent**. El Builder te guía paso a paso:

1. ❓ **What do you want your agent to do?**: elegir una [[📦 Plantillas de agente preconfiguradas|plantilla preconfigurada]] **(buena práctica: ya trae subagentes, acciones y variables)** o describir **rol, tipo de empresa, tareas** y lo crítico del trabajo. Lo que elijas define los subagentes y acciones.
2. 🏷️ **Name your agent**: un nombre descriptivo.
3. 🚀 **Let's Go**: se asocian los subagentes y acciones y el agente **ya funciona**. Si Agentforce pregunta algo, respondes; o **Skip Ahead** para llenarlo tú.

> [!example]- 🖼️ Los pasos guiados
> ![[builder-paso-que-hara-el-agente.jpg]]
> ![[builder-paso-nombre.png]]
> ![[builder-new-agent-prompt.jpg]]
> ![[builder-crear-chateando.jpg]]
> ![[builder-agente-inicial.jpg]]

## 🧩 Las 7 áreas
![[agentforce-builder-areas.jpg]]

| | Área | Para qué |
|---|------|----------|
| 1️⃣ | 🗺️ **Explorer** | Navegar todos los elementos: subagentes, acciones, configuración |
| 2️⃣ | 📝 **Canvas** | Editor tipo documento |
| 3️⃣ | 👁️ **Preview** | Probar con mensajes y ver el **resumen del razonamiento** (ver [[🧪 Probar un agente en el Builder]]) |
| 4️⃣ | 🔀 **Canvas / Script** | Cambiar entre lenguaje natural y código |
| 5️⃣ | 🤖 **Agentforce Assistant** | Ayuda a construir y **depurar** |
| 6️⃣ | 💾 **Save** | Guardar la versión actual (borrador) |
| 7️⃣ | 🔒 **Commit Version** | Foto **bloqueada** de la metadata, para activarla (ver [[🏷️ Versiones de un agente]]) |

## 🎨 Personalizar el agente
Desde el **Explorer** se editan (detalle en [[🗺️ Explorer del Agentforce Builder]]):
- ⚙️ **Settings**: nombre, descripción, **idiomas** en que responde, **instrucciones** de cómo interactuar con los usuarios y **mensajes de bienvenida y de error** con la voz de tu marca
- 🗂️ [[🗂️ Subagentes]] e instrucciones
- ⚡ [[⚡ Acciones de agente|Acciones]]: se agregan desde la **Asset Library** o se crean nuevas. Ver [[🔩 Configurar una acción custom]]
- 🔣 **Variables**
- 📚 **Fuentes de datos**

> 💡 En **Conversation Preview** prueba escenarios para los que el agente **fue diseñado y para los que no**, para ver cómo reacciona.

**Canvas** (por defecto, low-code) resume el Agent Script en **bloques** fáciles de leer, con **inline actions** para agregar **lógica determinística** (if/else) y un **selector de recursos** (subagentes, acciones, variables). **Script** es para control pro-code.

![[builder-canvas-subagente.jpg]]

> [!example]- 🖼️ Inline actions en Canvas
> ![[builder-inline-actions.jpg]]

> 💡 **Las dos vistas están siempre sincronizadas**: si editas en Canvas con lenguaje natural, el Builder escribe el Agent Script por detrás.

> ⚠️ Ojo de examen: ¿dónde se agrega un **if/else** sin código? → **inline actions** en **Canvas**. ¿Dónde se configuran **idiomas, mensajes de bienvenida y de error**? → **Settings** del agente. ¿Mejor práctica al crear? → **partir de una plantilla preconfigurada**.

> [!example]- 🖼️ Cloud Kicks en el Builder (con sus subagentes)
> ![[agentforce-builder-cloud-kicks.jpg]]

## 🔁 Repaso #flashcards
¿Cómo se llega a Agentforce Builder?::App Launcher → Agentforce Studio → Agents → New Agent.
¿Qué 5 novedades trae el nuevo Agentforce Builder?::Más determinismo (Atlas basado en grafos), control programático (Agent Script), asistencia integrada, UI mejorada (Explorer basado en archivos) y previews con trazas.
¿Qué se puede personalizar desde el Explorer?::Settings (nombre, descripción, idiomas, instrucciones, mensajes de bienvenida y error), subagentes, acciones (Asset Library), variables y fuentes de datos.
¿Cuáles son los pasos guiados para crear un agente?::What do you want your agent to do? (plantilla o descripción) → Name your agent → Let's Go.
¿Qué pasa con el Agent Script si editas en Canvas?::El Builder lo escribe por detrás; Canvas y Script siempre están sincronizados.
¿Cómo se agrega lógica determinística sin código en el Builder?::Con inline actions (if/else) en la vista Canvas.
