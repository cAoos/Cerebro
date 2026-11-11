---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-06
---
# 💬 Desplegar un agente en Enhanced Web Chat

La "puerta de entrada": un **chat en el sitio web**. Cuando el cliente hace clic, el **inbound flow** lo conecta al agente (ver [[🔀 Enrutamiento Omni-Channel de un agente]]). Se arma con **cuatro piezas**: canal **Enhanced Web Chat**, **pre-chat form**, **Embedded Service Deployment** y un sitio de **Experience Cloud**.

## 1️⃣ El canal
**Setup → Messaging Settings → New Channel → Start →** tipo **Enhanced Chat**:
- Nombre *Help Center Chat*, deployment type **Web**, dominio = el de **Experience Cloud Sites** (página **Domains**).
- Routing type **Omni-Flow**, el flow de enrutamiento al agente y la **fallback queue** (Messaging).
- Marcar **inactividad automática** e **identificar el idioma preferido** del usuario.
- **Parameter Mappings**: *First Name* → `firstName`, *Last Name* → `lastName`, *Email* → `email`. Unen el pre-chat con las **variables del inbound flow**.

![[despliegue-dominio-sites.jpg|400]]

## 2️⃣ Pre-chat y Embedded Service Deployment
Al crear el canal, Salesforce crea un **Embedded Service Deployment**. **Setup → Embedded Service Deployments → Help_Center_Chat → Edit Pre-Chat →** activar el **pre-chat** con First Name, Last Name y Email (los dos últimos obligatorios) **→ Publish**.

El **pre-chat form** recoge datos **antes** de la conversación, así el agente **empieza con contexto** y un cliente que ya existe se **liga a su registro**.

![[despliegue-pre-chat.jpg|400]]

**Test Messaging** abre una página con el botón de chat para probarlo.

![[despliegue-test-messaging.jpg|400]]

## 3️⃣ El sitio de Experience Cloud
**Setup → All Sites → New →** plantilla **Help Center** (URL `help`). En **Experience Builder → Components →** arrastrar **Embedded Messaging** al footer **→ Publish**.

## 4️⃣ CORS
**Setup → Digital Experiences → Settings →** copiar el dominio. Luego **Setup → CORS → New →** `https://` + dominio. Si da problemas, agregar también `*.live-preview`.

> 🚨 Si te saltas el CORS, el chat **no carga** y **no hay ningún error visible** que explique por qué.

## 5️⃣ Probar el escalamiento
- **Sin reps disponibles**: pedir un humano → el agente dice que no hay reps y **ofrece crear un caso**; verificar que el caso existe.
- **Con un rep Online** (Service Console → Omni-Channel): pedir un humano → **aceptar** en el sidebar y responder desde la Messaging Session.

Qué pasa por dentro al escalar: [[🧑‍⚖️ Cómo decide Omni-Channel a quién asignar]]. Versión corta de un proyecto anterior: [[🌐 Desplegar un Service Agent en Experience Cloud]].

> ⚠️ Ojo de examen:
> - El **chat no carga y no hay error** → revisa el **CORS allowlist**.
> - El **pre-chat** da contexto y liga al cliente con su registro gracias a los **parameter mappings** hacia las variables del flow.
> - El chat entra al sitio con el componente **Embedded Messaging**.
> - El **Embedded Service Deployment** se crea solo con el canal y hay que **publicarlo**.

## 🔁 Repaso #flashcards
¿Qué cuatro piezas se necesitan para poner un agente en un chat web?::Canal Enhanced Web Chat, pre-chat form, Embedded Service Deployment y un sitio (Experience Cloud).
El chat del agente no carga en el sitio y no hay mensaje de error. ¿Qué revisas?::El CORS allowlist: el dominio del sitio debe estar en Allowed Origins.
¿Para qué sirven los Parameter Mappings del canal de mensajería?::Conectan los campos del pre-chat form con las variables del inbound Omni-Channel flow.
¿Para qué sirve el pre-chat form?::Recoge datos (nombre, email) antes de la conversación para dar contexto al agente y ligar al cliente con su registro.
¿Qué componente agrega el chat al sitio de Experience Cloud?::Embedded Messaging.
¿Qué routing type se elige en el canal para enviar al agente?::Omni-Flow, con el flow de enrutamiento y una fallback queue.
