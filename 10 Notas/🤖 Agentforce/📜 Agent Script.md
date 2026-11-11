---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 📜 Agent Script

**Script del agente** es **el lenguaje para crear agentes** en Agentforce. Combina la **flexibilidad del lenguaje natural** con la **fiabilidad de las expresiones de programación**.

- 🔀 **Razonamiento híbrido**: lo determinístico (reglas que se cumplen siempre) + lo creativo del LLM.
- 🛤️ El agente puede seguir **una ruta definida y predecible** cuando el negocio lo exige.
- 🧠 Es lo que usa el [[🌍 Atlas Reasoning Engine]] para separar **el flujo de trabajo** del agente de sus **habilidades conversacionales**.
- 🖊️ En [[🏗️ Agentforce Builder]] se ve en la **vista Script**, con resaltado de sintaxis y validación en tiempo real.

## 🧪 Ejemplo
Regla: *"Nunca procesar una devolución de más de 30 días."* Con solo lenguaje natural, el LLM **probablemente** la cumple. Con Agent Script, una **expresión programática** la evalúa **antes** de hablar con el LLM, así que se cumple **siempre**.

> ⚠️ Ojo de examen: si piden **predecibilidad** o que una regla de negocio **se cumpla siempre** → Agent Script / instrucciones **programáticas** (determinísticas), no solo instrucciones en lenguaje natural.

Ver [[🌟 Características de Agentforce]] (predicción). Los bloques de un script completo y cómo se importa están en [[🧾 Estructura de un Agent Script]].

## 🖼️ Canvas y Script View
| Vista | Para quién | Qué ofrece |
|---|---|---|
| 📝 **Canvas** | Low-code | Resume el script en **bloques**. Con **`/`** insertas patrones como **if/else**; con **`@`** agregas subagentes, acciones y variables. Puedes editar en **lenguaje natural** |
| 💻 **Script View** | Pro-code | Editor del **Agent Script crudo** con resaltado, **autocompletado** y **validación en línea** |

Las dos editan **el mismo agente** y están **sincronizadas**.

**Template expressions**: en instrucciones y lógica se insertan valores con expresiones, como `{!@variables.order_id}` o `{!@actions.Get_Order}`, y se escriben **condiciones if/else**, **transiciones** entre subagentes y asignaciones de **variables**. Así lo determinista queda en código y lo conversacional en el LLM (**razonamiento híbrido**).

> 🌐 Fuente: [Get Started with Agent Script](https://developer.salesforce.com/docs/ai/agentforce/guide/agent-script.html).

## 🔁 Repaso #flashcards
¿Qué es Agent Script?::El lenguaje para crear agentes en Agentforce; combina lenguaje natural con expresiones programáticas.
¿Qué es el razonamiento híbrido?::Combinar la predictibilidad de expresiones programáticas con la flexibilidad del LLM.
¿Qué diferencia hay entre Canvas y Script View?::Canvas resume el script en bloques editables (low-code, / para if/else, @ para recursos); Script View muestra el Agent Script crudo con autocompletado y validación. Editan el mismo agente.
¿Qué son las template expressions en Agent Script?::Expresiones como {!@variables.x} o {!@actions.Y} para usar valores, condiciones if/else, transiciones y variables dentro de instrucciones y lógica.
