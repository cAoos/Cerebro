---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 🌐 Desplegar un Service Agent en Experience Cloud

Versión completa (canal, pre-chat, CORS, escalamiento): [[💬 Desplegar un agente en Enhanced Web Chat]].
Atajo con setup guiada desde Salesforce Go: [[🆘 Help Agent]] · [[🛠️ Crear un Help Agent paso a paso]].

Pasos del proyecto de Coral Cloud para poner un [[🎧 Agentforce Service Agent]] en un sitio de **Experience Cloud**:

| # | Paso | Dónde |
|---|---|---|
| 0️⃣ | **Activar Agentforce Studio** | Setup → **Salesforce Go** → buscar Agentforce Studio → Get Started → Turn On |
| 1️⃣ | **Publicar el sitio** | Setup → **All Sites** → Builder → Publish |
| 2️⃣ | **Crear el agente** | App Launcher → Agentforce Studio → **New Agent**, describirlo, nombrarlo y asignar un **usuario de agente** (EinsteinServiceAgent User) que **gestiona su acceso**. Ver [[🏗️ Agentforce Builder]] |
| 3️⃣ | **Commit + Activate** | En el Builder. Ver [[🏷️ Versiones de un agente]] |
| 4️⃣ | **Publicar el deployment** | Setup → **Embedded Service Deployments** → ESA Web Deployment → **Publish** (hasta ~10 min) |
| 5️⃣ | **Enrutar al agente** | Setup → Flows → **Route to ESA** (flow Omni-Channel) → Route To: **Agentforce Service Agent** + el agente → **Save As New Version** → **Activate** |
| 6️⃣ | **Agregar el chat al sitio** | Experience Builder → Components → **Embedded Messaging** → arrastrar → Publish |

![[deploy-route-to-esa.jpg]]

🧑‍💼 El **usuario asignado al agente** define **a qué datos tiene acceso**. Ver [[🔑 Mínimo privilegio en agentes]].

> 💡 Si el agente no aparece como opción en el flow, **no está activado**. Si no responde en el sitio, **republicar el sitio**.

> ⚠️ Ojo de examen: el canal web usa **Embedded Service Deployment** + componente **Embedded Messaging**. El tráfico llega al agente con un **flow de enrutamiento** (Route To = Agentforce Service Agent). El agente debe estar **activo** para elegirlo.

## 🔁 Repaso #flashcards
¿Cómo se activa Agentforce Studio en una org?::Setup → Salesforce Go → Agentforce Studio → Get Started → Turn On.
¿Qué controla el usuario que se asigna a un agente al crearlo?::El acceso del agente a los datos.
¿Qué hay que publicar para llevar el agente al canal web?::El Embedded Service Deployment.
¿Cómo se envían las conversaciones al nuevo agente?::Con el flow de enrutamiento (Route to ESA): Route To = Agentforce Service Agent y el agente elegido; guardar como nueva versión y activar.
¿Qué componente agrega el chat del agente a un sitio de Experience Cloud?::Embedded Messaging.
¿Por qué un agente no aparecería en el flow de enrutamiento?::Porque no está activado.
