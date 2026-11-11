---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 💼 Headless en ventas

**Problema:** antes de cada llamada, el vendedor salta entre Salesforce, correo y mensajería para armar el estado del negocio. La info está en Salesforce, pero encontrarla toma tiempo.

**Headless:** el vendedor le pregunta a **Slackbot** *"¿cuáles son mis mejores negocios que cierran este trimestre?"* y recibe la respuesta **sin entrar a Salesforce**. Salesforce sigue haciendo el trabajo; solo que es invisible.

## 🔌 Dos MCP servers trabajando juntos
Separar **dónde ocurre la conversación** de **dónde viven los datos**:

| MCP | Aporta |
|-----|--------|
| #️⃣ **Slack MCP Server** | **Contexto conversacional**: mensajes, canales, canvases. En qué trabaja el vendedor y con quién habla |
| ☁️ **Salesforce-Hosted MCP Server** | **Datos y lógica de Agentforce Sales** como endpoints, sin UI |

```text
🗣️ "¿Cómo va Acme?" ─► #️⃣ Slack MCP (contexto) ─► ☁️ Salesforce MCP (datos en vivo) ─► 💬 respuesta en el chat
```

## 🧰 Herramientas de Agentforce Sales por MCP
- 📋 **Opportunity Summary**: etapa, monto, fecha de cierre, siguientes pasos.
- ❤️ **Account Health**: estado, casos abiertos, actividad reciente, señales de renovación.
- ✍️ **Activity Logging**: registrar una llamada o cambiar la etapa **desde Slack**, con escritura en Salesforce en tiempo real.
- 📈 **Pipeline Summary**: foto del pipeline por etapa, riesgo y fecha, **sin correr un reporte**.

## 🎯 Grounding con actividad real
Usa **Momentum**, construido sobre **Einstein Activity Capture** y **Einstein Conversation Insights**:
- 📧 **Email and Calendar Sync**: sincroniza correos y reuniones (Gmail, Outlook) y los asocia solos a la oportunidad o cuenta.
- 🎙️ **Call Intelligence**: analiza grabaciones de llamadas y saca menciones de competidores, objeciones de precio, siguientes pasos y tareas.

Así, *"¿qué hablamos en la última llamada?"* se responde con **lo que pasó de verdad**, no solo con lo que se registró a mano.

> ⚠️ Ojo de examen: Slack MCP = **contexto de la conversación**; Salesforce-Hosted MCP = **datos confiables**. Cada llamada respeta la lógica y los guardrails de Salesforce ([[🚪 Open access, not open bypass]]).

Parte de [[🔓 Headless en Salesforce (AIforce)]] · ver [[🔌 MCP en Salesforce]].

> 📆 El ciclo completo en Slack (prospecting, nurturing, pipeline, account planning, metodología): [[📆 Ciclo de venta en Slack con headless]].

## 🔁 Repaso #flashcards
¿Qué aporta cada MCP en el caso de ventas headless?::Slack MCP: contexto conversacional; Salesforce-Hosted MCP: datos y lógica de Agentforce Sales.
¿Cuáles son las 4 herramientas MCP de Agentforce Sales?::Opportunity Summary, Account Health, Activity Logging, Pipeline Summary.
¿Con qué se aterriza el agente de ventas en la actividad real?::Con Momentum, sobre Einstein Activity Capture (correo y calendario) y Einstein Conversation Insights (análisis de llamadas).
