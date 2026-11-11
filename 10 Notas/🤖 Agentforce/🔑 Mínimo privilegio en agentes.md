---
tipo: nota
tema: seguridad
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🔑 Mínimo privilegio en agentes

**Principio 2** de la [[🌳 Seguridad en capas de headless|seguridad headless]]: cada persona, app y agente recibe **solo el acceso que necesita para su tarea, y nada más**. La pregunta de diseño: *¿cuál es el permiso mínimo útil que necesita este usuario?* (como podar el árbol para hacerlo más fuerte).

## 🪪 1. Identidad: el quién
> 🎬 *"I'm sorry, Dave. I'm afraid I can't do that."* HAL (2001: Odisea del espacio) limita lo que hace según **quién** se lo pide.

| Diseño | Cómo funciona | Ejemplo |
|--------|---------------|---------|
| 👤 **User-context** | Respeta el acceso del **usuario final** | Dos reps preguntan lo mismo al agente y reciben **resultados distintos** porque ven registros distintos |
| 🤖 **Integration user** | Usa los permisos de una **cuenta dedicada** | Un agente que habla con otro agente, limitado por un permission set |

## 🚦 2. Sensibilidad y acceso
Clasifica los datos por impacto: 🟢 bajo · 🟡 medio · 🔴 alto. Expón **capacidades** para el caso de uso, **no acceso total**.

- 👁️ Empieza con **solo lectura** si no hace falta cambiar nada.
- 🎯 Devuelve solo los **objetos, campos y registros** necesarios.
- 🔎 Usa consultas **específicas**, no abiertas.
- ⚡ Prefiere una **acción concreta** a permisos amplios de edición.
- ✍️ Agrega escritura **solo después** de probar y aprobar el diseño de solo lectura.

## 🧪 Ejemplo
Un banco expone a su agente de servicio una operación **de solo lectura** que devuelve **estado y prioridad del caso**, sin campos de pago. Aunque el agente reciba **instrucciones maliciosas**, no puede llegar a esos datos: el mínimo privilegio se aplica **en la capa de API**.

## 🛡️ 3. Supervisión y guardrails
Agrega **fricción** a las acciones con consecuencias según su impacto: ver [[🎚️ Autoridad progresiva]].

## 🧪 4. Probar e iterar
- ✅ Probar mínimo privilegio = confirmar que **las peticiones no autorizadas fallan**.
- 🧫 En **sandbox**, con **la identidad real del usuario final**, **no con tu cuenta de admin**.
- 💻 El **Apex a medida** debe aplicar la seguridad explícitamente.
- 🌍 Los permisos de Salesforce solo gobiernan **los datos que salen**, no lo que hace con ellos una herramienta externa (ChatGPT, etc.). Revisa todo el ciclo de vida y las políticas del proveedor.

> ⚠️ Ojo de examen: probar con **el usuario final, no con el admin**. Y si el agente no necesita escribir → **read-only**.

## 🔁 Repaso #flashcards
¿Qué es el principio de mínimo privilegio?::Dar a cada persona, app o agente solo el acceso que necesita para su tarea, y nada más.
¿Diferencia entre diseño user-context e integration user?::User-context respeta el acceso del usuario final; integration user usa los permisos de una cuenta dedicada.
¿Con qué identidad se prueba el mínimo privilegio?::Con la del usuario final real, en sandbox; nunca con la cuenta de admin.
¿Los permisos de Salesforce controlan lo que hace un proveedor externo con los datos?::No, solo gobiernan los datos que salen; hay que revisar las políticas del proveedor.
