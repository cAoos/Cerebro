---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# 🆘 Help Agent

Un **agente de Agentforce** de autoservicio 24/7 para clientes que se monta con una **guided setup** en pocos clics, sin equipo de desarrollo. Sale de **Salesforce Go** y está construido sobre la plantilla de [[🎧 Agentforce Service Agent]]. Ver [[🧑‍🤝‍🧑 Tipos de agentes de Agentforce]].

**Para qué sirve:** desviar casos rutinarios, liberar a los reps para lo complejo y sacarle ROI a la documentación de ayuda que ya existe.

## 🤵 Lo que la guided setup monta por detrás
Al aceptar los términos, la setup hace de "conserje" y provisiona sola:

| Pieza | Qué crea |
|---|---|
| 🔑 **Prerrequisitos y licencias** | Activa **Data 360** y **Agentforce**, y asigna licencias (Community, Contact Center as a Service) |
| 📚 **Conocimiento** | Una [[📚 Agentforce Data Library]] (ADL) por defecto para los archivos subidos |
| 🔀 **Handoff** | Una **routing configuration** y un **flow de Omni-Channel** para escalar a reps. Ver [[🔀 Enrutamiento Omni-Channel de un agente]] |
| 💬 **Chat web** | **Enhanced Chat** y **Messaging for In-App and Web**: la interfaz visual del chat. Ver [[💬 Desplegar un agente en Enhanced Web Chat]] |
| 🧑‍💼 **Agent user** | Un **usuario dedicado** al agente: respeta el **sharing model** y solo ve lo que ese usuario puede ver. No se configura en la setup; se ajusta luego en Setup → Users. Ver [[🔑 Mínimo privilegio en agentes]] |

La setup **solo pide lo mínimo**: nombre, idioma, saludo de bienvenida e instrucciones. Simplifica el [[🏗️ Agentforce Builder]] completo.

## 📚 Grounding: una sola fuente
| Opción | Cómo funciona |
|---|---|
| 📰 **Salesforce Knowledge** | Muestra las **data categories** de los artículos publicados. Todas vienen **seleccionadas por defecto**; se desmarcan las que no van. Los artículos sin categoría salen en **Uncategorized** |
| 📎 **Upload Files** | Arrastrar documentos **públicos**. Formatos **PDF, DOCX y HTML**, unas **300 páginas** en total. Ideal para pymes **sin base de conocimiento formal** |

- Cada Help Agent soporta **una sola fuente de grounding**. Para cambiarla se vuelve a la página **Give Your Agent Context**.
- Subir archivos **no los publica** en el sitio, solo aterriza al agente. Aun así, **solo información pública**: nada de documentos de compliance internos, diagramas sensibles ni PII.
- Para fuentes de terceros adicionales, después se extiende con [[☁️ Data 360 para agentes]].

## 📡 Canales
Desde **Add to Channels** se agrega a **cualquier combinación** de canales, por ejemplo portal y voz a la vez.

![[help-agent-canales.png]]

| Canal | Qué hace |
|---|---|
| 💬 **Web Chat** | Para un sitio de ayuda que **ya existe**: el camino más rápido. Genera un **snippet JavaScript asíncrono**. Antes pide el **dominio** del sitio: el script **solo corre en ese dominio**; copiado a otro dominio, el agente no se activa |
| 🌐 **Help Portal** | Para quien **no tiene sitio**: crea un **Agentforce Customer Service Portal** de inicio con barra de prompt e interfaz de conversación. Es una **base, no un sitio listo para producción**: se extiende en Experience Builder |
| 🎙️ **Voice** | Saludo, tono de voz, número por defecto y ruta de escalamiento. Se integra con **Agentforce Contact Center** y partners de telefonía. Ver [[🎙️ Agentforce Voice]] |
| 📱 **WhatsApp y SMS** | Aparecen en Add to Channels. El texto del módulo también dice que los canales de terceros como WhatsApp **requieren configuración manual** fuera de la setup |

También se puede poner en un **Experience Site** con el componente **Embedded Messaging**. Ver [[🌐 Desplegar un Service Agent en Experience Cloud]].

## 🧭 Manage Agents
En la pestaña Help Agent → **Manage Agents** se ven todos los Help Agents, su **versión** y su **estado** (Draft, Active, Inactive). Desde ahí:
- crear más agentes para otras áreas;
- gestionar **versiones**: cada edición y redespliegue crea una nueva. Ver [[🏷️ Versiones de un agente]];
- abrir el agente en el **Agentforce Builder** para agregar acciones, topics e integraciones.

Es un agente de Agentforce normal: convive con los demás y se extiende con acciones, flows y Apex. **El escalamiento a un rep hay que revisarlo** igual que en cualquier agente. Ver [[📞 Canales y escalamiento de un agente]].

> ⚠️ Ojo de examen: Help Agent = **setup guiada desde Salesforce Go** que provisiona sola Data 360, ADL, Omni-Channel y Enhanced Chat. **Una sola fuente de grounding** (Knowledge **o** archivos PDF/DOCX/HTML, ~300 páginas). El snippet de Web Chat está **atado a un dominio**. El Help Portal es un **starter**, no un sitio de producción. El acceso del agente lo define su **agent user dedicado**.

> 🗣️ También se puede crear **conversando** con un coding agent: [[🛠️ Crear un agente conversando paso a paso]].

## 🔁 Repaso #flashcards
¿Desde dónde se activa y configura un Help Agent?::Desde Salesforce Go, con la guided setup (Turn On y luego Build a Help Agent).
¿Qué provisiona sola la guided setup del Help Agent?::Data 360 y Agentforce, licencias (Community, Contact Center as a Service), una Agentforce Data Library, routing y flow de Omni-Channel, y Enhanced Chat / Messaging for In-App and Web.
¿Qué datos ve un Help Agent?::Los que puede ver su agent user dedicado, que se crea solo y respeta el sharing model.
¿Cuántas fuentes de grounding soporta un Help Agent?::Una sola: Salesforce Knowledge o archivos subidos.
¿Qué formatos y cuánto volumen acepta Upload Files?::PDF, DOCX y HTML, unas 300 páginas en total.
¿Qué data categories de Knowledge usa el agente por defecto?::Todas vienen seleccionadas; se desmarcan las que no van. Los artículos sin categoría salen en Uncategorized.
¿Subir archivos al Help Agent los publica en el sitio web?::No, solo aterrizan al agente. Aun así deben ser información pública.
¿Por qué Web Chat pide un dominio antes de dar el snippet?::Por seguridad: el JavaScript solo corre en ese dominio; en otro, el agente no se activa.
¿Qué es el Help Portal de la guided setup?::Un Agentforce Customer Service Portal de inicio, con barra de prompt y conversación; base que se extiende en Experience Builder, no un sitio listo para producción.
¿Qué estados muestra Manage Agents?::Draft, Active e Inactive, junto con la versión de cada agente.
¿Qué pasa cada vez que se edita y redespliega un Help Agent?::Se crea una nueva versión.
