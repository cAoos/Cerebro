---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-08
---
# 📮 Agentforce SDR (Engagement agent)

El agente de ventas que **atiende leads, contacts y person accounts** en todos los canales. En el setup actual aparece como plantilla **Engagement** (el diagrama del módulo aún dice *Lead Nurturing*). Panorama SDR frente a Sales Coach en [[💸 Agentforce for Sales]].

## 🎯 Qué hace
- 🚪 **Primer contacto** de los leads entrantes.
- ✉️ **Outreach personalizado** por email y **nudges** (recordatorios) si no responden.
- ❓ **Responde preguntas** y 📅 **agenda reuniones** a nombre del vendedor.
- 🔄 Más allá del negocio nuevo: **onboarding, renovaciones y reactivar oportunidades estancadas**.
- 📊 El equipo sigue su actividad en el **Control Center** y el dashboard **Agent Analytics**.

## 🧩 De qué depende
| Pieza | Para qué |
|---|---|
| **Einstein Activity Capture (EAC)** + **Salesforce Inbox** | Conectar email y calendario para enviar correos y agendar |
| **Data 360** + [[📚 Agentforce Data Library]] | Grounding con conocimiento de la empresa (FAQ, políticas, producto) |
| **Agent user** | El agente **corre como un usuario de Salesforce** con los permisos para trabajar con datos y hacer tareas que un usuario normal quizá no puede (ver [[🔐 Permisos del usuario del agente]]) |
| **Permission sets** | **Use Engagement Agent** (vendedores que trabajan con él) · **Configure Engagement Agent** (quién lo configura; el admin lo recibe solo al activar Agentforce) |

## ⚙️ Qué se configura en el agente
| Paso del wizard | Qué define |
|---|---|
| **Getting Started** | Agent user, nombre del agente, **nombre y descripción de la empresa** |
| **Email Settings** | **Primary Value Proposition** y **Key Achievements** (no se citan literal, guían el mensaje) · **Require Manual Approval** (el dueño del registro aprueba cada correo) · **Send as Seller** (identidad y horario del dueño) · **Nudge Settings**: un recordatorio al día hasta un máximo de intentos · tono |
| **Agent Knowledge & Data** | Elegir la data library; un archivo puede tardar **hasta 24 h** en aparecer en las respuestas |
| **Qualification Settings** *(opcional)* | **Qualification Status** activo · **Customer Profile** (el perfil de cliente ideal: industria, señales de intención de compra) · **Additional Data to Capture** (campos como Industry o Rating) |
| **Review and Activate** | Probar outreach, nudges y respuestas en Preview → **Activate Agent** |

> ⚠️ Ojo de examen: sin data library el agente responde con su **entrenamiento general**; con la FAQ cargada responde **preciso y on-brand**. **Qualification Settings** sirve para **priorizar** los prospectos con más potencial según el perfil de cliente ideal.

Montaje con [[🏁 Salesforce Go]] · práctica: [[🛠️ Configurar Agentforce SDR paso a paso]].

## 🔁 Repaso #flashcards
¿A qué registros atiende el agente SDR (Engagement)?::Leads, contacts y person accounts.
¿Qué hace el SDR más allá del negocio nuevo?::Ayuda con onboarding, renovaciones y reactivar oportunidades estancadas.
¿Dónde siguen los vendedores la actividad del agente SDR?::En el Control Center y el dashboard Agent Analytics.
¿Con qué funcionalidades trabaja el Engagement agent?::Einstein Activity Capture, Salesforce Inbox y Data 360.
¿Qué permission set necesita un vendedor para trabajar con el SDR?::Use Engagement Agent.
¿Qué permission set permite configurar el SDR?::Configure Engagement Agent; el admin lo recibe automáticamente al activar Agentforce.
¿Qué se define en Email Settings del SDR?::Primary Value Proposition, Key Achievements, aprobación manual, enviar como vendedor, nudges y tono.
¿Qué hace Require Manual Approval en el SDR?::El agente redacta los correos y el dueño del registro los aprueba antes de enviarlos.
¿Para qué sirve Qualification Settings?::Para evaluar prospectos con un Customer Profile y priorizar los de más potencial; es opcional.
¿Cuánto puede tardar un archivo de la data library en aparecer en las respuestas?::Hasta 24 horas.
¿Por qué cargar una FAQ al SDR?::Sin ella responde con entrenamiento general; con ella responde preciso y on-brand.
