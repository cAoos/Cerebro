---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-27
---
# 🚧 Guardrails para agentes autónomos

No importa la industria: un [[🦾 Agentes autónomos|agente autónomo]] actúa solo, así que necesita **precauciones bien definidas**.

| | Guardrail | En la práctica | 🤖 En Agentforce |
|---|-----------|----------------|------------------|
| 🗺️ | **Define Clear Boundaries** | Qué puede y qué no puede hacer | **Subagents** (antes *topics*) con alcance e **instructions** |
| 🔒 | **Implement Robust Security Measures** | Acceso mínimo a datos y sistemas | Permisos del usuario del agente · [[🛡️ Einstein Trust Layer]] |
| 👀 | **Monitor and Audit** | Revisar lo que hace y por qué | Audit trail · analítica del agente |
| 🧑‍🤝‍🧑 | **Integrate Human Oversight** | Una persona revisa o recibe los casos difíciles | **Escalar a un humano** |
| 🪟 | **Ensure Transparency** | Que el usuario sepa que habla con IA y cómo decide | Mensajes de bienvenida y avisos de IA |
| 🧪 | **Test Thoroughly** | Probar escenarios, incluidos los malos, antes de producción | **Testing Center** |
| 🔁 | **Continuous Learning and Improvement** | Ajustar con el feedback y los resultados | Feedback · iterar subagents e instructions |

> 💡 La supervisión humana es el [[🤝 Modelo de colaboración humano-IA]] aplicado a agentes. Contra usuarios que intentan saltarse los límites está la [[🧱 Defensa del prompt]].

> ⚠️ Ojo de examen: si preguntan cómo **limitar lo que un agente puede hacer** → subagents (topics), instructions y permisos. Si preguntan qué hacer cuando **el agente no puede resolver** → escalar a un humano.

> [!note]- 🌐 Complementado
> La columna *En Agentforce* no viene en la unidad: es el mapeo de cada guardrail a la herramienta de Agentforce, para el examen.

## 🔁 Repaso #flashcards
¿Cuáles son los 7 guardrails para agentes autónomos?::Define Clear Boundaries, Implement Robust Security Measures, Monitor and Audit, Integrate Human Oversight, Ensure Transparency, Test Thoroughly, Continuous Learning and Improvement.
¿Con qué se definen los límites de un agente en Agentforce?::Con subagents (antes topics), instructions y los permisos del usuario del agente.
¿Dónde se prueba un agente antes de producción?::En el Testing Center de Agentforce.
