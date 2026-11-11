---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-08
---
# 🏋️ Agentforce Sales Coach

Da **feedback personalizado por oportunidad** sobre el mensaje y la comunicación del vendedor. Resuelve tres dolores: un vendedor que se va y otro que tarda en arrancar, un junior que no sabe negociar con un cliente difícil y un **manager sin tiempo** para revisar cada deal y dar 1:1. Comparación con el SDR en [[💸 Agentforce for Sales]].

## 🎁 Qué ofrece
- ⏰ **Coaching autónomo bajo demanda**, sin un coach en vivo.
- 🎤 **Practicar el pitch** antes de la reunión, con feedback según el deal y su etapa.
- 🎭 **Role-plays** con IA: el agente simula al **cliente o comprador**.
- 📝 **Feedback personalizado** tras cada role-play.

## 🧩 Qué trae de fábrica
| Subagente | Para qué |
|---|---|
| **Opportunity Coaching** | Da el **feedback** tras un role-play o práctica de pitch |
| **Negotiation/Review Role-Play** | Simula al cliente en la negociación |
| **Proposal Quote Role-Play** | Simula al cliente en la propuesta o cotización |

Cada uno viene con descripción, scope e instrucciones de buenas prácticas. Además existe un subagente **Off Topic que no se puede desactivar**.

**5 etapas soportadas**, cada una con **su prompt template** y criterios propios: **Qualification, Needs Analysis, Discovery, Proposal/Pricing y Negotiation/Review**. En Prompt Builder se ve qué datos del CRM usa cada plantilla y qué preguntas espera que responda el vendedor.

![[coach-prompt-calificacion.jpg]]

## 🖱️ Cómo lo ve el vendedor
Componente **Agentforce Sales Coach** en la página de la **oportunidad**, con tarjetas por etapa:

| Tarjeta | Etapa |
|---|---|
| Review Your Knowledge of this Opportunity | Qualification |
| Practice Your Pitch | Needs Analysis |
| Role Play With Your Coach | Proposal/Pricing Quote |
| Sharpen Your Negotiation Skills | Negotiation/Review |

![[coach-menu-etapas.jpg]]

## 🔌 Funcionalidades requeridas
| Pieza | Para qué |
|---|---|
| **Agentforce** | Configurar y gestionar agentes |
| **Einstein Generative AI** | Mover las prompt templates que generan el feedback |
| **Agentforce Studio** | Subagentes, acciones, role-play y feedback |
| **Data 360** | Alojar archivos y dar **RAG** |

> ⚠️ Ojo de examen: los **subagentes e instrucciones** guían el role-play, pero el **feedback lo genera el prompt**: ahí están el grounding, los **criterios de evaluación** y el **formato** del feedback. Para cambiar *cómo actúa el comprador* se tocan instrucciones; para cambiar *qué evalúa el feedback* se toca el prompt.

Montaje: [[🛠️ Configurar Agentforce Sales Coach paso a paso]] · ajustes: [[🎨 Personalizar Agentforce Sales Coach]].

> 🎤 Cómo se practica (pitch con video, role-play por voz, límites de 5 min y 3 intercambios): [[🎤 Practicar con Agentforce Sales Coach]].

## 🔁 Repaso #flashcards
¿Qué da Agentforce Sales Coach?::Feedback personalizado y específico del deal sobre el mensaje y la comunicación del vendedor.
¿Cuáles son los 3 subagentes de fábrica de Sales Coach?::Opportunity Coaching, Negotiation/Review Role-Play y Proposal Quote Role-Play.
¿Qué subagente de Sales Coach da el feedback?::Opportunity Coaching.
¿Qué subagentes simulan al cliente en Sales Coach?::Negotiation/Review Role-Play y Proposal Quote Role-Play.
¿Cuáles son las 5 etapas de oportunidad que soporta Sales Coach?::Qualification, Needs Analysis, Discovery, Proposal/Pricing y Negotiation/Review.
¿Qué tiene cada etapa soportada por Sales Coach?::Su propia prompt template con criterios y preguntas de esa etapa.
¿Qué genera el feedback de Sales Coach: las instrucciones o el prompt?::El prompt, que tiene el grounding, los criterios de evaluación y el formato.
¿Para qué usa Sales Coach Data 360?::Para alojar archivos y dar RAG.
¿Qué 4 funcionalidades requiere Sales Coach?::Agentforce, Einstein Generative AI, Agentforce Studio y Data 360.
¿Dónde usa el vendedor Sales Coach?::En el componente Agentforce Sales Coach de la página de la oportunidad.
¿Qué subagente de Sales Coach no se puede desactivar?::Off Topic.
