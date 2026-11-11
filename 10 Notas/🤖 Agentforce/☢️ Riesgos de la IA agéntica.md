---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# ☢️ Riesgos de la IA agéntica

Cuanto más **autónomo** es el sistema, más crece el potencial de **mal uso** y de **consecuencias no previstas**. Los 6 riesgos clave:

| Riesgo | Qué es |
|---|---|
| 💣 **Unintended Consequences** | Acciones autónomas con resultados inesperados: contenido **sesgado u ofensivo**, **decisiones incorrectas**, interacciones fuera de las guías éticas |
| 🔐 **Security and Privacy** | Los agentes manejan datos sensibles; sin diseño seguro hay **fuga inadvertida** de datos |
| ⚖️ **Ethical and Legal Considerations** | Los agentes deben cumplir **políticas y leyes** |
| 🕹️ **Loss of Human Control** | Con más autonomía, cuesta **mantener la supervisión** → errores, faltas éticas, daño reputacional |
| 🤖 **Automation Bias** | El usuario **confía de más** en la IA y asume que siempre acierta; **RAG lo agrava** porque la respuesta suena **autoritativa** aunque esté mal |
| 🚫 **Increased User Misuse** | Más usuarios → más uso malicioso o equivocado (contenido inapropiado, violar privacidad) |

**Mitigación de Salesforce:** [[🏛️ Guardrails de plataforma y de Agentforce|guardrails]] en la plataforma y el producto, **pruebas adversariales** con [[🎯 Red-teaming de IA|red-teaming]], la **AI Acceptable Use Policy** y la posibilidad de **personalizar los guardrails** con los valores y requisitos de cumplimiento de tu organización.

Ver [[🌟 IA agéntica confiable]] y, para riesgos en general, [[🧯 Mitigación de riesgos de IA]].

> ⚠️ Ojo de examen: **automation bias** = confiar de más en la IA, y **RAG lo empeora** porque hace que la respuesta parezca más creíble. No confundir con **user misuse** (el usuario usa la IA mal a propósito o por error).

## 🔁 Repaso #flashcards
¿Cuáles son los 6 riesgos clave de la IA agéntica?::Unintended consequences, security and privacy, ethical and legal considerations, loss of human control, automation bias e increased user misuse.
¿Qué es el automation bias?::Que el usuario confía de más en la salida de la IA y asume que siempre es correcta.
¿Qué técnica puede aumentar el automation bias y por qué?::RAG, porque hace que las respuestas parezcan muy autoritativas y creíbles aunque estén mal.
¿Qué estrategias usa Salesforce para mitigar los riesgos de la IA agéntica?::Guardrails en plataforma y producto, red-teaming, la AI Acceptable Use Policy y guardrails personalizables.
