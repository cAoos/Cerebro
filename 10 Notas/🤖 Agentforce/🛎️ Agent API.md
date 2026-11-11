---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[2026-10 Agentforce Specialist]]"
creada: 2026-11-08
---
# 🛎️ Agent API

API REST para **conversar con un agente de Agentforce desde fuera de Salesforce**, sin su UI: abrir sesión, enviar mensajes y recibir respuestas.

## 🎯 Cuándo usarla
| Caso | Ejemplo |
|---|---|
| 📱 **Experiencia propia** | Una app web o móvil custom con su propio chat |
| ⚙️ **Automatización headless** | Un proceso batch o un sistema que le pide al agente que razone y actúe |
| 🌐 **Plataformas externas** | Llamar al agente desde otro sistema o canal no soportado de forma nativa |
| 🤝 **Agente a agente** | Invocar un agente de Agentforce desde otro agente |

## 🔐 Cómo se conecta
- **External Client App** con el flujo **client credentials**.
- **Run As user** con al menos acceso **API Only**: ese usuario decide qué ve y qué puede hacer el agente.
- Scopes que citan las guías: `api`, `refresh_token`/`offline_access`, `chatbot_api`, `sfap_api`.
- **No** soporta agentes de tipo **Agentforce (Default)**.

> ⚠️ Ojo de examen: si piden **integrar un agente en una UI propia o en otro sistema** → **Agent API**. Si piden que una herramienta externa (Claude, Cursor) **use datos y acciones de Salesforce con la identidad de cada usuario** → **MCP** con OAuth y PKCE ([[🛫 Checklist antes de conectar herramientas headless]]). Si es un canal soportado (chat web, voz, Slack) → una **conexión** del agente ([[🔌 Conexiones y canales de un agente]]).

> [!note]- 🌐 Fuentes
> [Agent API Developer Guide](https://developer.salesforce.com/docs/ai/agentforce/guide/agent-api.html) · [Get Started](https://developer.salesforce.com/docs/ai/agentforce/guide/agent-api-get-started.html). Los scopes vienen de guías de terceros: confírmalos en la doc.

## 🔁 Repaso #flashcards
¿Para qué sirve la Agent API?::Para conversar con un agente de Agentforce desde fuera de Salesforce, sin su UI.
¿Cuándo usar Agent API?::En experiencias web o móviles propias, automatizaciones headless, plataformas externas o para invocar un agente desde otro agente.
¿Qué flujo de autenticación usa la Agent API?::Client credentials en una External Client App, con un Run As user (mínimo API Only).
¿Qué decide lo que puede ver y hacer un agente llamado por Agent API?::El Run As user de la External Client App.
¿Qué tipo de agente no soporta la Agent API?::Agentforce (Default).
¿Agent API frente a MCP?::Agent API para hablar con un agente desde otra app; MCP para que una herramienta externa use datos y acciones de Salesforce como el usuario.
