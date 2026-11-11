---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-08
---
# 🪟 Cuatro pilares técnicos de headless

Headless **desacopla la plataforma** (la org con datos e inteligencia) **de la interfaz** (donde se interactúa con ella). La lógica, los datos y el gobierno siguen **centralizados en Salesforce**; lo que cambia es **cómo y dónde** se accede. Cuatro pilares lo hacen posible:

| | Pilar | Qué es | Ejemplo en ventas |
|---|---|---|---|
| 🧬 | **Metadata** | Cómo Salesforce **entiende tu proceso**: schemas, campos, picklists, **validation rules, flows**, configuraciones y el **sales path** | Antes de pasar de Proposal a Negotiation, el agente confirma que es la siguiente etapa, que ninguna validation rule lo bloquea (Amount, Close Date) y sabe que Negotiation suma al forecast **Commit** |
| 🔌 | **MCP / API** | Los **puentes seguros**: **+60 herramientas MCP** para consultar, actualizar, traer reportes y ejecutar acciones, **respetando permisos y sharing** | El agente en Slack corre un SOQL del pipeline; un cambio de etapa pasa por el **REST API** de registros, el mismo que usa una página Lightning |
| ⚡ | **Skills** | **Prompt templates reutilizables y prearmados** que se ejecutan **con un clic** | En vez de escribir *"muéstrame mis 10 mejores deals"*, se llama la skill **View Top Opportunities** |
| 🖼️ | **Headless Experience Layer (HXL)** | El **motor de renderizado** que pinta datos y flujos en cualquier interfaz | Un mismo widget *review pipeline suggestions* se ve nativo en Slackbot, Claude, ChatGPT y Agentforce sin reescribir la lógica |

> ⚠️ Ojo de examen: **no confundir** con los [[🧲 Pilares de valor de headless]] (Adoption, Reach, Speed, AI agent strategy). Estos cuatro son **técnicos**: Metadata, MCP/API, Skills y HXL. El agente se apoya en la metadata **en vez de asumir un proceso genérico**.

## 🌐 Superficies donde funciona
| Superficie | Quién y para qué |
|---|---|
| 💻 Entornos de desarrollo | Devs y admins construyen y automatizan con IA conversacional en **Claude Code, Cursor** y extensiones de IDE |
| 💬 Colaboración | Equipos de venta actúan sobre oportunidades en **Slack y Microsoft Teams** |
| 🤖 IA conversacional | Datos y flujos por lenguaje natural en **ChatGPT y Gemini** |
| 📱 Apps móviles | Vendedores de campo consultan el pipeline y actualizan registros |
| 🧩 Apps custom | Interfaces a medida para flujos especializados |

Herramientas concretas en [[🧳 Headless Toolkit]] · casos en [[📆 Ciclo de venta en Slack con headless]].

## 🔁 Repaso #flashcards
¿Cuáles son los 4 pilares técnicos de headless?::Metadata, MCP/API, Skills y Headless Experience Layer (HXL).
¿Qué significa headless en términos de arquitectura?::Desacoplar la plataforma (datos e inteligencia) de la interfaz donde se usa.
¿Qué aporta la metadata a un agente de ventas?::El proceso real de la empresa: etapas, validation rules, flows y efectos como el forecast, en vez de un proceso genérico.
¿Cuántas herramientas MCP ofrece Salesforce para agentes?::Más de 60, respetando permisos y sharing rules.
¿Qué son las skills en los pilares de headless?::Prompt templates prearmados y reutilizables que se ejecutan con un clic.
¿Qué es la Headless Experience Layer?::El motor de renderizado que muestra datos y flujos de Salesforce de forma nativa en cualquier interfaz.
¿Qué API usa un cambio de etapa hecho desde Slack?::El REST API de registros, el mismo que usa una página Lightning.
¿Cuáles son las 5 superficies donde funciona headless?::Entornos de desarrollo, herramientas de colaboración, IA conversacional, apps móviles y apps custom.
