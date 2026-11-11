---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# 🛠️ Crear un Help Agent paso a paso

Proyecto de Coral Cloud Resorts del módulo *Agentforce Help Agent*. El concepto está en [[🆘 Help Agent]].

## 1️⃣ Activar Help Agent
1. ⚙️ → **Salesforce Go** → buscar **Help Agent**.
2. **Get Started** → **Turn On** → **Turn On** en el popup. La setup provisiona Data 360, ADL, Omni-Channel y Enhanced Chat.

## 2️⃣ Definir la identidad
1. En **Build and Manage Your Agents**, **Go** junto a **Build a Help Agent** → **Get Started**.

![[help-agent-build-go.jpg]]

2. Agent Name **Help Agent**, idioma **English**, **saludo de bienvenida** y revisar las **Agent Instructions** → **Continue**.

![[help-agent-identidad.jpg]]

El **agent user** se crea solo por detrás.

## 3️⃣ Darle contexto (grounding)
1. En **Give Your Agent Context** → **Upload Files** → subir *CoralCloudResortsFAQs.pdf*. Crea la entrada **Help Agent Data Library**.
2. ⏳ **Esperar a que el estado sea Ready** antes de seguir. Si se da Continue antes, la siguiente unidad no funciona.

![[help-agent-archivos-ready.jpg]]

## 4️⃣ Canal: Help Portal
1. En **Add to Channels** → **Manage** bajo Help Portal.
2. Site Name **CCHelpPortal**, ajustar colores → **Create and Deploy**.
3. ⏳ Esperar a que el portal esté **Ready** y aparezca su URL → **Continue**.

![[help-agent-portal-url.jpg]]

## 5️⃣ Probar en el portal
1. En la sección Channels, abrir el link de **CCHelpPortal**.
2. Preguntar en **Ask me anything** lo que está en el PDF: hora de check-out, mascotas, costo de cancelar dentro de 7 días.
3. 📎 El agente **cita sus fuentes por defecto**: **Sources** muestra el link al PDF.
4. 🧪 **Probar los límites**: una pregunta fuera del PDF. Un agente bien aterrizado **declina con cortesía u ofrece pasar a un rep**, en vez de alucinar.

## 6️⃣ Canal: Experience Site
1. Setup → **All Sites** → **Builder** junto a coral-cloud → **Publish**.
2. Components → arrastrar **Embedded Messaging** al sitio.
3. En el menú del componente, **Embedded Web Deployment** → elegir el deployment del Help Agent.

![[help-agent-embedded-messaging.png]]

4. **Publish** otra vez → **View coral-cloud** → botón **Ask Me Anything** abajo a la derecha.

## 7️⃣ Después
Help Agent → **Manage Agents**: versiones, estados y salto al [[🏗️ Agentforce Builder]] para extenderlo. Revisar el **escalamiento a un rep**. Ver [[🧑‍⚖️ Cómo decide Omni-Channel a quién asignar]].

> ⚠️ Ojo de examen: el orden es **identidad → contexto → canales**. Hay que **esperar Ready** en la carga de archivos y en el portal. Para el Experience Site se usa **Embedded Messaging** apuntando al **Embedded Web Deployment** del Help Agent, y el sitio hay que **publicarlo**.

## 🔁 Repaso #flashcards
¿Cuáles son los tres pasos de la guided setup del Help Agent?::Meet Your Agent (identidad), Give Your Agent Context (grounding) y Add to Channels.
¿Qué hay que esperar antes de dar Continue tras subir archivos?::Que el estado de Upload Files sea Ready.
¿Cómo muestra el Help Agent de dónde sacó una respuesta?::Cita sus fuentes por defecto: Sources muestra el link al documento.
¿Qué debe hacer un agente bien aterrizado ante una pregunta fuera de su conocimiento?::Declinar con cortesía u ofrecer pasar a un rep, sin alucinar.
¿Cómo se pone el Help Agent en un Experience Site existente?::Componente Embedded Messaging en Experience Builder, elegir el Embedded Web Deployment del Help Agent y publicar el sitio.
