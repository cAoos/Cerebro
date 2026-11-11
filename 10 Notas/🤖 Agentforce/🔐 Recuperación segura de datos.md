---
tipo: nota
tema: trust-layer
estado: nueva
debil: false
fuente: "[[2026-10 Agentforce Specialist]]"
creada: 2026-11-09
---
# 🔐 Recuperación segura de datos

Cuando una plantilla o un agente trae datos de Salesforce para el grounding, lo hace **con los permisos del usuario que ejecuta**: respeta permisos de objeto, **FLS** y reglas de sharing. Si el usuario no puede ver un campo, el LLM tampoco lo recibe.

- 🤖 En un agente, el "usuario que ejecuta" es el del contexto: el empleado en un agente de empleado, o el **agent user** (Run As) en un agente de servicio o en la Agent API. Ver [[🛂 Accesos en un proyecto de Agentforce]] y [[🔑 Mínimo privilegio en agentes]].
- 📭 Consecuencia típica: **el dato no llega y el LLM deja un placeholder o lo omite**.

## 🧪 Ejemplo
Un comercial genera un Sales Email y el borrador sale con *"[Cargo del destinatario]"*. La plantilla está bien; el comercial no tiene **FLS** sobre el campo Title del contacto, así que el dato no se recuperó.

> ⚠️ Ojo de examen: "El resultado sale con placeholders o le faltan datos a **un** usuario" → **le falta acceso a los campos** (FLS/permisos). Si les pasa a todos, sospecha del grounding de la plantilla.

Parte de [[🛡️ Einstein Trust Layer]] · Guía: [[🛡️ Trust Layer para el examen]]

## 🔁 Repaso #flashcards
¿Con qué permisos recupera datos la Trust Layer para el grounding?::Con los del usuario que ejecuta: respeta permisos de objeto, FLS y sharing.
Un borrador generado sale con placeholders solo para un usuario: ¿causa probable?::El usuario no tiene acceso (FLS) a los campos que usa la plantilla.
