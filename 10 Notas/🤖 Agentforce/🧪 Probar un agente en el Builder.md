---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 🧪 Probar un agente en el Builder

Probar es esencial para tener un agente **de confianza**. Se hace en el panel **Preview** de [[🏗️ Agentforce Builder]], que tiene **dos modos**:

| | Modo | Qué hace | ⚠️ Riesgo |
|---|------|----------|-----------|
| 🧫 | **Simulate** | Valida la **configuración** del agente **sin revisar permisos, sin ejecutar acciones y sin tocar datos** | Ninguno |
| 🔴 | **Live Test** | **Ejecuta las acciones y hace cambios** en la org, para ver cómo se comporta activo | Cambia datos reales |

## 🔍 Herramientas para entender el resultado
![[builder-preview-simulate.jpg]]

- 📋 **Interaction details**: resumen del razonamiento de cada mensaje (actual y pasados), con **explicaciones generadas por IA**.
- 🧵 **Trace**: los **pasos** que hizo el agente; puedes pedirle a Agentforce que te explique cualquier paso.
- 🔣 **Variables**: seguir el valor de cada variable durante la conversación.
- ⏱️ **Tiempo por subproceso**: para **reducir la latencia**.
- 💬 Chatear con Agentforce para **corregir el agente** según lo que encontraste.

![[builder-preview-trace.png]]

## 🧪 Ejemplo
Linda prueba *"¿dónde está mi pedido?"* en **Simulate**: el trace muestra que eligió el subagente equivocado. Ajusta las instrucciones y repite. Cuando funciona, pasa a **Live Test** para confirmar que la acción realmente consulta el pedido **con los permisos**.

> ⚠️ Ojo de examen: probar **sin permisos ni acciones ni datos** → **Simulate**. Probar **ejecutando acciones de verdad** → **Live Test**. ¿Por qué un agente tarda? → **tiempo por subproceso** en el trace.

Más allá del Builder: **Agentforce Testing Center** para pruebas en lote (ver [[🤖 Agentforce]]).

> 🪄 Excepción: **Service Assistant no se prueba en el Builder ni en Testing Center**, sino redactando un plan en la página del Case.

> ✔️ Cómo evalúa Testing Center (assertions de subagente, acción y resultado con LLM juez): [[✔️ Evaluaciones de Testing Center]].

## 🔁 Repaso #flashcards
¿Cuáles son los 2 modos del Preview del Builder?::Simulate (sin permisos, acciones ni datos) y Live Test (ejecuta acciones y cambia la org).
¿Qué modo de prueba no ejecuta acciones ni revisa permisos?::Simulate.
¿Qué muestra el trace en el Preview?::Los pasos que hizo el agente, los valores de las variables y el tiempo de cada subproceso.
