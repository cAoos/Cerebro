---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# 🧳 Headless Toolkit

Es lo que hace posible [[🔓 Headless en Salesforce (AIforce)|AIforce]]: abre la arquitectura de Salesforce, **con su seguridad y gobierno**, a cualquier agente de terceros. En vez de entrar por el navegador, se accede a la org, los datos y la metadata con **cuatro herramientas**:

| Herramienta   | Qué es                                                                                                                      | Cuándo usarla                                                                                         |
| ------------- | --------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| 🔌 **MCP**    | Conector universal, estándar abierto, autenticación **OAuth**, varios tipos de servidor que respetan el modelo de seguridad | Dejar que un **agente de IA actúe sobre una org** de forma segura. Ver [[🔌 MCP en Salesforce]]       |
| 🛰️ **API**   | Endpoints **robustos y deterministas** para ejecutar tareas **sin navegador**                                               | **Integrar** Salesforce con sistemas de terceros por código. Ver [[🛰️ Enfoque API-first]]            |
| ⌨️ **CLI**    | Acceso a Salesforce desde una **terminal** o cualquier interfaz de IA, **scriptable**                                       | **Automatizar** tareas de desarrollo o despliegue con scripts. Ver [[⌨️ Salesforce CLI]]              |
| 🎒 **Skills** | Expertise de dominio empaquetada en **comandos reutilizables y componibles**                                                | Darle a un agente **flujos repetibles** con resultados consistentes. Ver [[🎒 Anatomía de una skill]] |

**Dónde se usan:** IDEs y asistentes como **Claude, Cursor, ChatGPT, Agentforce Vibes** y **Slack**.

> ⚠️ Ojo de examen: las cuatro herramientas son **MCP, APIs, CLIs y Skills**. Agente que actúa sobre la org → **MCP**. Integración sistema a sistema → **API**. Scripts de despliegue y CI/CD → **CLI**. Flujo multipaso repetible en un solo comando → **Skill**.

> 🧑‍💻 Quien usa estas herramientas desde Claude Code o Cursor: [[🧑‍💻 Coding agents en Salesforce]].

## 🔁 Repaso #flashcards
¿Qué es el Salesforce Headless Toolkit?::Lo que hace posible AIforce: abre la arquitectura, la seguridad y el gobierno de Salesforce a cualquier agente de terceros.
¿Cuáles son las cuatro herramientas del Headless Toolkit?::MCP servers, APIs, CLI y Skills.
¿Cuándo usar MCP dentro del Headless Toolkit?::Para que un agente de IA actúe sobre una org de forma segura, con OAuth y el modelo de seguridad de Salesforce.
¿Cuándo usar APIs dentro del Headless Toolkit?::Para integrar Salesforce con sistemas de terceros por código, con endpoints deterministas sin navegador.
¿Cuándo usar la CLI dentro del Headless Toolkit?::Para automatizar tareas de desarrollo o despliegue con scripts.
¿Cuándo usar Skills dentro del Headless Toolkit?::Para darle a un agente flujos multipaso repetibles en un solo comando, con resultados consistentes.
