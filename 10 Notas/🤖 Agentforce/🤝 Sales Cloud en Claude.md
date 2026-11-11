---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🤝 Sales Cloud en Claude

La experiencia de ventas de Salesforce **dentro de Claude Cowork**, aterrizada en el contexto del CRM. El vendedor investiga cuentas, revisa oportunidades o arma un close plan **sin abrir Salesforce** ni saltar entre pestañas.

## 🧩 La familia Claude
![[claude-chat-vs-cowork.png]]

| Producto | Para qué |
|----------|----------|
| 💬 **Claude** | Compañero conversacional: preguntas e ideas en un chat |
| 🗂️ **Claude Cowork** | **Espacio de trabajo agéntico** en la app de escritorio: le das un objetivo y hace **el trabajo completo** (busca, razona, planea, actúa) mientras tú mantienes el control |
| 💻 **Claude Code** | Agente para desarrolladores: construir, depurar y mantener software |
| 🤝 **Sales Cloud in Claude** | La experiencia de ventas de Salesforce sobre esas capacidades agénticas |

## ⚙️ Cómo funciona
- 🔌 Usa el **plugin Headless 360 for Sales**, que funciona sobre el **Headless 360 MCP server** (ver [[🧭 Herramientas del Headless 360 MCP]]).
- 🌉 Conecta Cowork con: ☁️ Salesforce CRM · 📧 Gmail · 📅 Google Calendar · 📁 Google Drive · #️⃣ Slack. Cada espacio se **autoriza primero**.
- 📦 **Skills prediseñadas**: prompts empaquetados que ya saben **qué datos traer y qué acciones tomar**.
- 🔒 Los datos pasan por los **permisos existentes del usuario**, sin logins extra.
- 🎯 Une **IA probabilística** con **verdad determinística**: el razonamiento se aterriza en datos, metadatos, procesos, lógica de negocio y permisos en vivo.

## 🧰 Las 5 skills de ventas
| Skill | Qué resuelve |
|-------|--------------|
| 🏆 **account-tiering** | Clasifica tu cartera contra el **ICP** usando cuentas, oportunidades, llamadas y correos |
| 📈 **pipeline-review** | Vista por etapa de cobertura, antigüedad y negocios en riesgo |
| 📋 **call-prep** | Brief automático: roles de asistentes, sentimiento, historial y preguntas de discovery |
| ✉️ **call-follow-up** | Convierte la transcripción en correo de seguimiento listo + resumen para Slack |
| 🗺️ **account-plan** | Close plan formal con CRM + investigación web; lo **revisas y confirmas antes de que se sincronice** a Salesforce |

> ⚠️ Ojo de examen: las acciones con consecuencias son **human-in-the-loop / approval-gated**: Claude propone, el vendedor confirma (ver [[🎚️ Autoridad progresiva]]).

Es el mismo patrón de [[💼 Headless en ventas]], pero en Claude en vez de Slack. Parte de [[🔓 Headless en Salesforce (AIforce)]].

## 🔁 Repaso #flashcards
¿Qué es Claude Cowork?::Un espacio de trabajo agéntico en la app de escritorio de Claude que completa trabajos de varios pasos a partir de un objetivo.
¿Qué conecta Sales Cloud in Claude con Cowork?::El plugin Headless 360 for Sales, sobre el Headless 360 MCP server.
¿Cuáles son las 5 skills de Sales Cloud in Claude?::account-tiering, pipeline-review, call-prep, call-follow-up, account-plan.
¿Qué une el Headless 360 MCP server según Salesforce?::La IA probabilística con la verdad determinística de Salesforce (datos, lógica y permisos).
