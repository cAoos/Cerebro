---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 🕷️ Amenazas de seguridad para agentes

Los agentes **actúan, no solo analizan**, y eso cambia los riesgos:
- **Riesgos de IA tradicional** (data poisoning, prompt injection, alucinaciones): afectan la **integridad de los datos** y **lo que el modelo dice**.
- **Riesgos de agentes**: van un paso más allá, porque esa salida **dispara acciones reales** (mandar mensajes, cambiar registros, actualizar sistemas). El impacto llega rápido a la **operación**: una factura equivocada a un cliente, una nómina que no corre, un reporte de cumplimiento generado pero nunca enviado.

![[amenazas-agentes-riesgos-humanos-sistema.jpg|400]]

## 🔟 Riesgos comunes (adaptados de OWASP, agentic AI)
| Riesgo | Causa e impacto |
|---|---|
| 🧠 **Memory poisoning** | Siembran **contexto falso** en la memoria corta/larga → el agente **repite acciones inseguras** en el tiempo |
| 🔧 **Tool misuse** | Engañan al agente para **abusar de sus herramientas autorizadas** (enviar datos, encadenar acciones) **dentro de sus permisos** |
| 🔓 **Privilege compromise** | Una **mala configuración** le da **más acceso del previsto** → aprueba, cambia o borra |
| 🌊 **Resource overload** | **Inundan de tareas** al agente → se agota cómputo o **cuota de API** y el proceso se frena |
| 🌀 **Cascading hallucinations** | El agente **reutiliza salidas falsas** propias o de otros agentes y el error se **propaga** |
| 🎭 **Misaligned/deceptive behaviors** | Persigue el objetivo por **vías prohibidas**: **parece cumplir pero hace daño** |
| 👻 **Repudiation and untraceability** | Sabotean los **logs** o los llenan de registros incompletos → **imposible auditar** o responder al incidente |
| 🪪 **Identity spoofing and impersonation** | Se hacen pasar por un **usuario o agente** para dar órdenes con identidad de confianza |
| 😵 **Overwhelming human-in-the-loop** | **Saturan de aprobaciones** al humano → aprueba sin mirar por **fatiga de decisión** |
| 🕸️ **Human attacks on multiagent systems** | Explotan la **delegación y confianza entre agentes** para escalar privilegios o saltarse controles |

Consecuencias: interrupción operativa, pérdida de confianza, daño reputacional, problemas legales y financieros. Vengan de **diseño, configuración, ejecución o ataque**, el efecto es el mismo: **el agente hace algo que el negocio no quería**. Para encontrarlos a tiempo: [[🔬 Threat modeling de flujos con agentes]]. Quién ataca y por qué: [[🦹 Actores de amenaza y sus motivaciones]].

Relacionado: [[☢️ Riesgos de la IA agéntica]], [[🧱 Defensa del prompt]], [[🔑 Mínimo privilegio en agentes]].

> ⚠️ Ojo de examen: distingue **tool misuse** (abusa de herramientas **dentro** de sus permisos) de **privilege compromise** (tiene **más** permisos de los debidos por mala configuración). **Overwhelming HITL** = fatiga de aprobaciones. **Repudiation** = sin logs no hay trazabilidad.

## 🔁 Repaso #flashcards
¿En qué se diferencian los riesgos de agentes de los riesgos de IA tradicional?::Los de IA tradicional afectan datos y salida del modelo; los de agentes llevan esa salida a acciones reales en la operación.
¿Qué es memory poisoning en un agente?::Sembrar contexto falso en su memoria para que repita acciones inseguras con el tiempo.
¿Qué diferencia hay entre tool misuse y privilege compromise?::Tool misuse abusa de herramientas dentro de los permisos autorizados; privilege compromise es tener más acceso del previsto por mala configuración.
¿Qué es resource overload?::Inundar al agente de tareas hasta agotar cómputo o cuota de API y frenar los procesos.
¿Qué son las cascading hallucinations?::Cuando agentes reutilizan salidas falsas propias o de otros agentes y el error se propaga por los flujos.
¿Qué es overwhelming human-in-the-loop?::Saturar de revisiones al humano para que apruebe acciones riesgosas por fatiga de decisión.
¿Qué es repudiation and untraceability?::Sabotear o saturar los logs para que las acciones del agente no se puedan rastrear ni auditar.
¿De qué fuente se adaptan los riesgos comunes de agentes del módulo?::De la guía de OWASP sobre agentic AI (Agentic AI – Threats and Mitigations).
