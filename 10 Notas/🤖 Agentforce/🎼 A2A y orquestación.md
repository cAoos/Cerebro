---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🎼 A2A y orquestación

| | Concepto | Qué es |
|---|----------|--------|
| 🤝 | **A2A (agent to agent)** | Un agente **le pasa el trabajo directo a otro**, automáticamente y **sin un humano en medio**. Crea un solo flujo continuo, sin esperas |
| 🎼 | **Orquestación** | Coordinar **varios agentes y sistemas** para completar una tarea compleja: cada agente toca su parte, en el orden y momento correctos, como en una orquesta con su director |

- 🧩 Salesforce trae **orquestación entre productos** integrada: los agentes trabajan entre Agentforce Service, Agentforce Sales, Data 360 y sistemas externos **sin "pegamento" de código a medida**.

## 🧪 Ejemplo
Un agente de servicio detecta que el cliente quiere ampliar su contrato y le pasa el caso (**A2A**) al agente de ventas. La **orquestación** asegura que primero se consulte el perfil en Data 360, luego se cotice y al final se avise en Slack.

> ⚠️ Ojo de examen: A2A es el **traspaso entre agentes**. El **traspaso a un humano** es otra cosa (ver [[🌍 Atlas Reasoning Engine]]).

## 🏗️ ¿Cuándo conviene una arquitectura multi-agente?
| ✅ Conviene | ❌ No conviene |
|---|---|
| Dominios **distintos** con dueños, datos o permisos propios (facturación, RR. HH., soporte) | Un solo dominio con pocas acciones |
| Un agente con **demasiados subagentes o acciones** que se confunde | Cuando un subagente más resuelve el problema |
| Hay que **escalar** por partes y **controlar** cada agente por separado (versiones, pruebas, permisos) | Cuando la latencia y el costo de varios saltos no se justifican |
| El trabajo cruza **sistemas o agentes externos** | Una integración determinista simple (mejor una API) |

Patrón típico: un **agente orquestador** recibe la solicitud y **delega** en agentes especialistas.

| Protocolo | Para qué |
|---|---|
| 🔌 **MCP** (Model Context Protocol) | Que un agente use **herramientas y datos** externos |
| 🤝 **A2A** (Agent2Agent) | Que un agente **delegue en otro agente**, incluso de otra plataforma. Salesforce fue socio de lanzamiento |
| 🛰️ **API** | Integraciones **deterministas**, sin razonamiento |

> ⚠️ Ojo de examen: herramienta externa → **MCP**. Otro agente que razona → **A2A**. Llamada fija y predecible → **API**. Ver [[🔌 MCP en Salesforce]] y [[🛎️ Agent API]].

## 🔁 Repaso #flashcards
¿Qué es A2A?::Agent to agent: un agente le pasa el trabajo directamente a otro, sin intermediario humano.
¿Qué es la orquestación de agentes?::Coordinar varios agentes y sistemas para que cada uno haga su parte en el orden y momento correctos.
¿Cuándo conviene una arquitectura multi-agente?::Con dominios distintos (dueños, datos, permisos), agentes sobrecargados o necesidad de escalar y controlar cada parte por separado.
¿Para qué sirven MCP y A2A?::MCP: que un agente use herramientas y datos. A2A: que un agente delegue en otro agente.
