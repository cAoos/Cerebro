---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# 🛫 Checklist antes de conectar herramientas headless

Conectar la primera herramienta o agente externo exige **preparación deliberada**, no solo activar algo.

| | Área | Qué hacer |
|---|------|-----------|
| 🔐 | **Setup y autenticación** | Activar el servidor en **Setup > Salesforce Hosted MCP Servers** · crear una **External Client App** con el scope **`mcp_api`**, OAuth 2.0 con **PKCE** |
| 👤 | **Integration user y permisos** | Revisar sus **permission sets** y su lugar en la **role hierarchy** · aplicar **FLS** para ocultar campos sensibles en todo perfil conectado a herramientas |
| 🧼 | **Metadata** | Labels y descriptions de objetos de alto tráfico · labels, descriptions y help text de campos clave · picklists sin abreviaturas (ver [[🧼 Metadata como capa de grounding]]) |
| 🧯 | **Manejo de errores** | Apex, flows y validation rules con **mensajes de error explícitos**, no excepciones genéricas del sistema |

## 🛡️ La seguridad no tiene atajo
Una herramienta programática **hereda** el mismo modelo que cualquier usuario:
- Cada transacción del MCP server **corre como el usuario autenticado**, acotada por la External Client App con `mcp_api`.
- Aplican **CRUD, FLS, sharing rules, perfiles y permission sets**.
- Todo queda **registrado y atribuido** a ese usuario en el audit trail.

> ⚠️ Ojo de examen: scope **`mcp_api`** + **OAuth 2.0 con PKCE** en una **External Client App**. Los hosted MCP servers vienen **apagados** hasta activarlos en Setup (ver [[🗄️ Tipos de MCP servers en Salesforce]]).

Relacionado: [[🚪 Open access, not open bypass]] · [[🔑 Mínimo privilegio en agentes]] · [[🪨 Data foundation para headless]].

## 🔁 Repaso #flashcards
¿Dónde se activa el Salesforce Hosted MCP Server?::En Setup > Salesforce Hosted MCP Servers.
¿Qué scope necesita la External Client App para MCP?::mcp_api.
¿Qué flujo de autenticación usa la conexión MCP?::OAuth 2.0 con PKCE, en una External Client App.
¿Con qué identidad corre cada transacción del MCP server?::Con la del usuario autenticado; aplican CRUD, FLS, sharing, perfiles y permission sets.
¿Qué hay que revisar del integration user?::Sus permission sets, su role hierarchy y FLS para ocultar campos sensibles.
¿Cómo deben fallar Apex, flows y validation rules para agentes?::Con mensajes de error explícitos y accionables, no excepciones genéricas.
¿Quién aparece en el audit trail de una acción hecha por MCP?::El usuario autenticado.
