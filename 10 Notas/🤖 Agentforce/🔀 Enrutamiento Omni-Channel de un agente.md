---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-06
---
# 🔀 Enrutamiento Omni-Channel de un agente

¿Cómo llega un mensaje del cliente **al agente**? ¿Y cómo pasa **a un humano** cuando el agente no puede? Con **dos flows de Omni-Channel**:

| Flow | Qué hace |
|---|---|
| 📥 **Inbound** | Cuando empieza una conversación, la **enruta al agente de IA** |
| 📤 **Outbound** | Cuando el agente **escala**, enruta la conversación del agente a una **cola de reps** |

## 🧱 Prerrequisitos
| Pieza | Para qué | Ejemplo |
|---|---|---|
| 📺 **Service Channel** | Une la routing configuration y los flows con el objeto **Messaging Session** | NTO Help Center |
| ⚖️ **Routing Configuration** | Cómo se **asignan** las sesiones de la cola a los reps | Priority 1 · **Least Active** · capacity **Inherited** · 25% |
| 👥 **Queue** | Adónde va la conversación si **no se puede enrutar al agente** o si el agente **escala** | Messaging (objeto Messaging Session) |

![[despliegue-service-channel.jpg|500]]
![[despliegue-routing-config.jpg|500]]

## 📤 Escalamiento (outbound)
El **Escalation subagent** dice **cuándo** escalar: el cliente **pide una persona**, el **sentimiento se vuelve negativo** o el pedido está **fuera del alcance** del agente. Entonces dispara el outbound flow:
- **Hay reps disponibles** → actualiza la sesión y usa la acción **Route Work** para mandar la sesión **con el historial** a la cola. El rep sigue donde quedó el agente y **el cliente no repite nada**.
- **No hay reps** → el agente **retoma la conversación** con el contexto previo y, por ejemplo, **ofrece crear un caso**.
- El escalamiento **se intenta una sola vez por sesión**.

![[despliegue-flow-outbound.jpg|500]]

**Conectarlo:** Builder → **Connections → Messaging → Settings → Escalation →** elegir el flow (debe estar **activo**) y editar el **mensaje de escalamiento** (*"One moment while I check if there are any reps available"*) **→ Save → Commit Version → Activate.**

## 📥 Entrada (inbound)
Recibe la **Messaging Session** y los datos del **pre-chat form**, **busca si el usuario es un contacto existente** y usa **Route Work** para mandarlo al agente. Si no se puede, lo manda a la **cola**.

![[despliegue-flow-inbound.jpg|500]]

> 💡 Si el agente **no está activo**, **no aparece** como opción de ruta en Flow Builder.

> 🧠 Caso práctico completo (candidatos, Least Active frente a Most Available, push, cola llena, sin reps): [[🧑‍⚖️ Cómo decide Omni-Channel a quién asignar]].

## 🧑‍💼 Preparar a los reps
- Cada rep es un **Service Resource**.
- Al menos **dos Presence Statuses** (disponible / no disponible).
- **Omni-Channel sidebar** y una página de Messaging Session en la **Service Console**.

> ⚠️ Ojo de examen:
> - **Inbound** lleva al agente; **outbound** saca del agente a la cola.
> - Las dos usan la acción **Route Work**.
> - Las tres piezas previas son **service channel, routing configuration y queue**.
> - Sin reps, el agente retoma la conversación; **un solo intento por sesión**.
> - El historial viaja con la sesión, así que el cliente **no repite**.

## 🔁 Repaso #flashcards
¿Qué hace el flow inbound de Omni-Channel en Agentforce?::Enruta una conversación nueva al agente de IA (y a la cola si no es posible).
¿Qué hace el flow outbound?::Escala la conversación del agente a una cola de reps humanos.
¿Qué tres prerrequisitos necesitan los flows de Omni-Channel para Messaging?::Service channel, routing configuration y queue.
¿Qué acción usan los flows para mandar el trabajo a un agente o una cola?::Route Work.
¿Cuándo escala el Escalation subagent?::Cuando el cliente pide una persona, el sentimiento se vuelve negativo o el pedido está fuera de su alcance.
¿Qué pasa si el agente escala y no hay reps disponibles?::Retoma la conversación con el contexto previo (p. ej. ofrece crear un caso); el escalamiento se intenta solo una vez por sesión.
¿Dónde se conecta el flow outbound al agente?::En el Builder: Connections → Messaging → Settings → Escalation.
¿Qué necesita un rep para recibir sesiones de mensajería?::Ser Service Resource, presence statuses y el Omni-Channel sidebar en la Service Console.
