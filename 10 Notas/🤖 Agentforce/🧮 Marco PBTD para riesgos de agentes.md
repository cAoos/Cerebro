---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-01
---
# 🧮 Marco PBTD para riesgos de agentes

Riesgos de los agentes autónomos: amenazas de seguridad, brechas de datos, daño reputacional, pérdida financiera, sesgo, **alucinaciones**, y problemas de transparencia y responsabilidad.

🛡️ Agentforce ayuda con **guardrails en lenguaje natural** (qué puede y no puede hacer el agente) y el [[🛡️ Einstein Trust Layer]] (detección de daño y toxicidad). Pero **no todos los guardrails están en la tecnología**: también hay **gobernanza** (ej: una **safety review** obligatoria es un **proceso de negocio**). Ver [[⚖️ Gobernanza de IA]] y [[🚧 Guardrails para agentes autónomos]].

💡 Abordar el riesgo **desde el inicio** no frena: **acelera**, porque evita que el proyecto se cancele y las lecciones se reusan en el siguiente caso.

## 🧮 People, Business, Technology, Data
![[planear-agente-marco-pbtd.png]]

| Categoría | Consideraciones | Riesgos (Coral Cloud) |
|---|---|---|
| 👥 **People** | Empoderamiento (roles, capacitación) · cultura (diseño centrado en humanos, gestión del cambio, adopción) | **Rechazo** del cliente · **abuso**/manipulación · **cultura**: miedo a perder empleos |
| 💼 **Business** | Valor (KPIs) · operaciones (estructura, procesos, gobernanza, DevOps) | **Fit** con los procesos · **reporting**: KPIs invalidados · **incentivos**/compensación · **escalamiento** poco claro · agente que no sigue políticas |
| 💻 **Technology** | Herramientas (infra, APIs, prompts, salvaguardas) · modelos (selección, costo) | **Precisión** (alucinaciones) · **confiabilidad** (variabilidad) · **auditoría** · **latencia** |
| 🗄️ **Data** | Calidad · estrategia | **Acceso** (permisos) · **privacidad** · **cumplimiento** (residencia de datos) · **fit for purpose** · **ética** (sesgo) |

## 🧯 Guardrails por categoría (ejemplos)
| Riesgo | Guardrails |
|---|---|
| 🙅 **Rechazo**: el cliente no confía | 👥 Estrategia de comunicación y educación · 💻 agente **transparente de que es IA** · 💻 **mensaje de bienvenida** que fija expectativas |
| 🔀 **Escalamiento** inconsistente | 💼 Definir **criterios y contexto** para escalar · 💻 pasar un **resumen de la interacción** al rep · 💻 en las **instrucciones**, palabras o peticiones que disparan el escalamiento |

📝 **Documentar** riesgos y guardrails (cumplimiento y auditorías) **y experimentar** en sandbox para validar que funcionan.

> ⚠️ Ojo de examen: el marco es **People, Business, Technology, Data**. Alucinaciones y latencia → **Technology**. KPIs invalidados e incentivos → **Business**. Rechazo y miedo al empleo → **People**. Permisos, privacidad, sesgo → **Data**. Cada riesgo se mitiga combinando guardrails de **varias** categorías.

## 🔁 Repaso #flashcards
¿Qué cuatro categorías usa el marco para hablar de riesgos de agentes?::People, Business, Technology y Data.
¿En qué categoría van las alucinaciones y la latencia?::Technology.
¿En qué categoría va que los KPIs del equipo queden invalidados por el agente?::Business.
¿En qué categoría va el rechazo del cliente a hablar con la IA?::People.
¿Qué guardrails ayudan si los clientes no confían en el agente?::Comunicación y educación, que el agente diga que es IA y un mensaje de bienvenida que fije expectativas.
¿Qué guardrails mejoran el escalamiento a humanos?::Criterios claros para escalar, pasar un resumen de la interacción al rep y describir en las instrucciones qué dispara el escalamiento.
¿Una safety review obligatoria es un guardrail técnico?::No: es un proceso de negocio de gobernanza.
