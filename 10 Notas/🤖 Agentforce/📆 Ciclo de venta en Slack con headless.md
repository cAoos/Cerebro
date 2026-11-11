---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-08
---
# 📆 Ciclo de venta en Slack con headless

**Problema** (Jordan Kim, Ursa Major Solar): empieza el día en Slack, toma notas en otra app, revisa el pipeline en una hoja de cálculo y a las 10 entra a Salesforce a **actualizar 12 oportunidades a mano**. Resultado: cambio de contexto, **pipeline desactualizado** y más tiempo en admin que vendiendo.

**Headless**: los datos e inteligencia de Salesforce **llegan a Slack** vía **Slackbot**, y los registros se actualizan sin entrar a la org.

## 🔄 Cinco etapas del ciclo
| | Etapa | Qué pide el vendedor | Qué obtiene |
|---|---|---|---|
| 🎯 | **Prospecting** | Reuniones de hoy con **fit score**, research brief, stakeholders, noticias y oportunidades previas · email de outreach < 150 palabras atado a una **señal de compra** | Un **prospecting agent** ya dejó cuentas de alto fit y reuniones agendadas |
| 🌱 | **Lead nurturing** | Quién respondió, estado **BANT** y siguiente mejor acción | Sugiere discovery call con 3 huecos del calendario; *"Book Tuesday 2 PM…"* envía la invitación y cambia el **lead status** |
| 📈 | **Pipeline management** | *"What deals need my attention today? Rank them by urgency…"* | Deal top, problema (14 días sin actividad), **riesgo alto** y acciones sugeridas |
| 🗺️ | **Account planning** | Estado del **account plan** y sus iniciativas | Detecta iniciativa estancada y **whitespace** (expansión donde no estás); crea tarea y **notifica al manager** |
| ✅ | **Cumplir la metodología** | *"Is this deal missing anything before the next stage?"* | Faltan budget y authority → revisa **transcripciones y correos**, los encuentra y, **tras confirmar**, actualiza los campos |

> ⚠️ Ojo de examen: el vendedor **revisa y aprueba** (edita el correo, confirma los campos BANT) antes de que algo se envíe o escriba. El valor está en no saltar entre herramientas ni investigar a mano.

## 👥 Para cada rol
| Rol | Desde dónde | Qué hace |
|---|---|---|
| 💻 Developers | Claude Code, Cursor | Consultar datos inline y desplegar config desde la línea de comandos |
| 🛠️ Admins | Slack, móvil | Configurar agentes, ajustar filtros y depurar comportamiento **sin laptop** |
| 📊 Sales leaders | Slack | Insights del pipeline y **alertas de coaching** sobre deals en riesgo |

Base: [[🪟 Cuatro pilares técnicos de headless]] · arquitectura con Slack MCP + Salesforce MCP en [[💼 Headless en ventas]] · BANT en el SDR: [[📮 Agentforce SDR (Engagement agent)]].

## 🔁 Repaso #flashcards
¿Cuáles son las 5 etapas del ciclo de venta headless en Slack?::Prospecting, lead nurturing, pipeline management, account planning y cumplimiento de la metodología de ventas.
¿Qué hace el prospecting agent antes de que el vendedor empiece el día?::Deja en Salesforce una lista de cuentas de alto fit y reuniones agendadas.
¿Qué criterios revisa el lead nurturing en Slack?::BANT: budget, authority, need y timing.
¿Cómo ayuda headless a cumplir la metodología de ventas?::Detecta campos faltantes (p. ej. budget, authority), los busca en transcripciones y correos y los actualiza tras confirmar.
¿Qué detecta el account planning en Slack además del estado de las iniciativas?::Oportunidades de whitespace (expansión) e iniciativas estancadas.
¿Cómo usan headless los admins?::Configuran agentes, ajustan filtros y depuran comportamiento desde Slack o el móvil.
¿Qué reciben los sales leaders en Slack?::Insights del pipeline y alertas de coaching sobre deals en riesgo.
¿Qué problema de productividad resuelve headless en ventas?::El cambio constante de herramientas y la carga manual que deja el pipeline desactualizado.
