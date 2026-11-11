---
tipo: nota
tema: seguridad
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🚪 Open access, not open bypass

**Principio 1** de la [[🌳 Seguridad en capas de headless|seguridad headless]]: una llamada headless desde Claude Code o cualquier agente externo **hereda exactamente el mismo gobierno** que una llamada tradicional. Cambia la conexión o la superficie; **el modelo de seguridad y los chequeos son idénticos**.

- 🔕 Los **Salesforce Hosted MCP Servers vienen deshabilitados por defecto**. El admin habilita explícitamente los que los agentes pueden usar: **nada se expone hasta que alguien lo decide**.
- 🪪 Cuando un agente pide un registro por [[🔌 MCP en Salesforce|MCP]], pasa por la **misma verificación de identidad, FLS y gobierno** que un usuario dando clic en la UI.

## 🔧 Detalles técnicos
- 🧩 Usa **External Client Apps (ECAs)**, **no Connected Apps**, con un scope OAuth dedicado: **`mcp_api`**.
- 🔐 Flujo de autorización: **OAuth 2.0 Authorization Code con PKCE** (Proof Key for Code Exchange).

## 🎛️ Tres herramientas para limitar lo que ve el agente
| | Herramienta | Qué hace |
|---|-------------|----------|
| 👁️ | **Read-only servers** | Exponen datos **sin escritura**: limitan el "radio de explosión" de un error del agente |
| 🔎 | **Named queries** | Consultas **parametrizadas** limitadas a lo que el agente necesita |
| ⚡ | **Custom Apex actions** | Exponen solo operaciones específicas, definidas como **`@InvocableMethod`** |

## 🧪 Ejemplo
Claude Code pide los casos de un cliente por MCP. Si el usuario que autorizó la conexión **no ve el campo `SSN__c`**, el agente **tampoco lo ve**. No hay atajo por ser "un agente".

> ⚠️ Ojo de examen: MCP de Salesforce usa **ECA + scope `mcp_api` + OAuth 2.0 con PKCE**. Los servidores están **apagados por defecto**.

> 🛫 En la práctica: scope `mcp_api`, OAuth con PKCE y transacciones como el usuario autenticado, en [[🛫 Checklist antes de conectar herramientas headless]].

## 🔁 Repaso #flashcards
¿Qué significa "open access, not open bypass"?::Que una llamada headless hereda exactamente la misma seguridad y gobierno que una llamada desde la UI de Salesforce.
¿Cómo vienen los Salesforce Hosted MCP Servers por defecto?::Deshabilitados; el admin habilita explícitamente cuáles pueden usar los agentes.
¿Qué usa el MCP de Salesforce para autorizar?::External Client Apps (no Connected Apps), scope mcp_api y OAuth 2.0 Authorization Code con PKCE.
¿Cuáles son las 3 herramientas para limitar lo que un agente hace por MCP?::Read-only servers, named queries y custom Apex actions (@InvocableMethod).
