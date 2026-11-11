---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# 🗄️ Tipos de MCP servers en Salesforce

En vez de construir una integración custom por cada herramienta de IA, **se configura un MCP server una vez** en Salesforce y cualquier cliente compatible (Claude, Cursor, Agentforce Vibes) se conecta con **OAuth**. Ver [[🔌 MCP en Salesforce]].

| Tipo | Qué es | Ejemplos |
|---|---|---|
| 🏢 **Salesforce-hosted standard** | Capacidades de plataforma listas para usar. **Autentican con la org** y exponen metadata, datos y funcionalidad | **Headless 360 MCP** (Beta), **Metadata Grounding MCP** (GA octubre 2026), Data 360 MCP |
| 📦 **Salesforce-hosted product** | Específicos de un producto, con **URL de servidor propia** | **Tableau Next MCP**, **MuleSoft MCP** |
| 🌍 **External** | De terceros: **registro e instalación manual**; aparecen como servidores externos en el **API Catalog** | — |
| 🧩 **Custom** | El admin **combina herramientas de varios servidores** en uno | Por persona, una **sola URL** con todo lo que necesita |

## 🏢 Reglas de los servidores hosted
- Vienen **preconfigurados** con un **set fijo de herramientas** que **no se puede modificar**.
- Están **desactivados por defecto**: los **activa un administrador**.
- **Autenticación por usuario**: cada llamada respeta **FLS, permisos de objeto y sharing rules**. El agente actúa **en nombre del usuario autorizado**, dentro del perímetro de seguridad. Ver [[🚪 Open access, not open bypass]].

## 🧩 Para qué un custom server
- **Agrupar** las herramientas que una persona necesita en **una sola URL**: el cliente MCP solo necesita esa.
- **Exponer herramientas propias** respaldadas por **Apex, Flows o APIs**, porque los estándar **no se pueden modificar**.

> ⚠️ Ojo de examen: ¿cómo agrego una herramienta propia (Apex o Flow) a MCP? → **custom MCP server**, porque los estándar son fijos. ¿Un MCP de terceros? → registro manual, aparece en el **API Catalog**. Los hosted vienen **apagados** hasta que un admin los activa.

> 🪐 Los que extienden la data foundation fuera de Salesforce (Informatica, MuleSoft, Tableau): [[🪐 Cross-cloud MCP servers]]. Cómo activarlos y autenticarse: [[🛫 Checklist antes de conectar herramientas headless]].

## 🔁 Repaso #flashcards
¿Qué cuatro tipos de MCP servers hay para clientes de Salesforce?::Salesforce-hosted standard, Salesforce-hosted product, external y custom.
¿Qué es un Salesforce-hosted standard MCP server?::Uno que empaqueta capacidades de plataforma, autentica con la org y da acceso a metadata, datos y funcionalidad (por ejemplo Headless 360 MCP o Metadata Grounding MCP).
¿Qué distingue a un Salesforce-hosted product MCP server?::Es específico de un producto y tiene su propia URL, como Tableau Next MCP o MuleSoft MCP.
¿Dónde aparecen los MCP servers externos y cómo se agregan?::En el API Catalog, con registro e instalación manual.
¿Para qué sirve un custom MCP server?::Para agrupar herramientas de varios servidores en una sola URL por persona y exponer herramientas propias con Apex, Flows o APIs.
¿Se pueden modificar las herramientas de un MCP server hosted por Salesforce?::No: tienen un set fijo; para herramientas propias se usa un custom server.
¿Cómo vienen los MCP servers hosted por Salesforce en una org?::Desactivados por defecto; un administrador los activa.
¿Qué seguridad aplican los MCP servers de Salesforce en cada llamada?::Autenticación por usuario, FLS, permisos de objeto y sharing rules.
