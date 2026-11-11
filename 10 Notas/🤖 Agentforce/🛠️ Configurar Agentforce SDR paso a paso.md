---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-08
---
# 🛠️ Configurar Agentforce SDR paso a paso

Ejercicio de la empresa ficticia **Welo** (soluciones de IT y data centers). Concepto en [[📮 Agentforce SDR (Engagement agent)]]; recorrido en [[🏁 Salesforce Go]].

## 1️⃣ Encender Agentforce
Engranaje → **Salesforce Go** → buscar **Agentforce for Sales** → tarjeta Turn On Agentforce → **Turn On**.

![[sdr-go-buscar.jpg]]
![[sdr-go-turn-on.png]]

## 2️⃣ Activar la plantilla Engagement
En *Start with an Agent Template*, activar **Engagement** → Turn On. La tarjeta muestra los pasos con links.

![[sdr-engagement-wizard.jpg]]

## 3️⃣ Accesos
**Manage Access for Managers and Users** → pestaña **Use Engagement Agent** → All Users → marcar al usuario → Assign. Para dar permiso de configurar a otros: pestaña **Configure Engagement Agent**.

![[sdr-acceso-usuarios.jpg]]

## 4️⃣ Einstein Activity Capture
**Go To Setup** → Start Set Up → Google → **User Level** → nombre de la conexión → revisar sync y advanced settings → agregar usuarios → Finish. Refrescar Salesforce Go (a veces más de una vez).

## 5️⃣ Agent user y email
**Manage Agent's User Record and Email** → **+ New User** (Sales Agent) → Create: la configuración necesaria se aplica sola. Si eliges un usuario existente, el setup **verifica que tenga los permisos**. Luego **Connect Account** para enlazar email y calendario (Inbox + EAC).

![[sdr-usuario-agente.jpg]]
![[sdr-conectar-email.jpg]]

## 6️⃣ Data library
**Configure Data for Your Agent** → **Add Data** → **Upload Files** → nombre *Welo Customer Policies Library* → subir la FAQ → Save. Esperar el estado **Uploaded**.

![[sdr-data-library.jpg]]

## 7️⃣ Construir el agente
**Build and Manage Agent → Go** (abre Agentforce Studio) → Get Started → plantilla **Engagement** → Continue.

![[sdr-build-go.png]]

| Paso | Qué se hace |
|---|---|
| **Getting Started** | User Record ya viene con el agent user · Agent Name *Lead Nurturing* · Company Name y descripción |
| **Email Settings** | Pegar value proposition y key achievements · elegir un lead → **Try it out** para ver el correo inicial |
| **Agent Knowledge & Data** | Elegir la data library · probar con otro lead |
| **Qualification Settings** | Activar Qualification Status · Customer Profile (financial services, intención de compra) · capturar **Industry** y **Rating** |
| **Review and Activate** | Revisar outreach, nudges y respuestas → **Activate Agent** |

![[sdr-getting-started.jpg]]
![[sdr-email-settings.jpg]]
![[sdr-knowledge-data.jpg]]
![[sdr-qualification.jpg]]
![[sdr-review-activate.jpg]]

> ⚠️ Ojo de examen: el orden es **Agentforce → plantilla → accesos → EAC → agent user y email → data library → construir**. Cada paso del wizard tiene **Preview** con un lead real para ver el correo antes de activar.

## 🔁 Repaso #flashcards
¿Dónde se activa Agentforce for Sales en el ejercicio?::En Salesforce Go, buscando Agentforce for Sales y pulsando Turn On.
¿Qué plantilla de agente se activa para el SDR?::Engagement.
¿Qué nivel se elige al configurar Einstein Activity Capture en el ejercicio?::User Level.
¿Qué pasa si eliges un usuario existente como agent user?::El setup verifica que tenga los permisos necesarios.
¿Para qué se conecta la cuenta de Google en el setup del SDR?::Para enlazar email y calendario a Salesforce vía Inbox y Einstein Activity Capture.
¿Cómo se prueba el correo inicial antes de activar el SDR?::En Preview Email, eligiendo un lead y pulsando Try it out.
¿Qué campos extra se capturan en Qualification Settings del ejercicio?::Industry y Rating.
¿Cuál es el último paso del wizard del SDR?::Review and Activate → Activate Agent.
