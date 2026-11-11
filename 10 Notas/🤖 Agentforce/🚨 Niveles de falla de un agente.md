---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 🚨 Niveles de falla de un agente

Salesforce usa una **taxonomía de puntos de falla** para medir **qué tan disruptiva** es una falla para el usuario. Pasa de "está roto" a "**exactamente por qué** el usuario está frustrado".

| Severidad | Nivel | Qué pasa |
|---|---|---|
| 🔴 **P0** | **Red Alert: System Failure** | La más grave. El agente **se cae, hace timeout** o da una **alucinación sin sentido** y peligrosa |
| 🟠 **P1** | **Missed the Mark: User Intent Not Met** | Funciona, pero la respuesta **no está alineada con el objetivo** del usuario: entendió mal el *qué* o el *porqué* |
| 🟡 **P2** | **Usable, Not Lovable: Limited User Value** | Funciona y es correcto, pero es de **baja calidad**, **muy verboso** o le deja **más trabajo** al usuario |

- Las **P0** se suelen atrapar en el **QA técnico**.
- Las **P1 y P2** son donde está el **riesgo de frustración y abandono**: difíciles de ver en pruebas tradicionales, obvias para el usuario final.

![[evaluacion-agente-p0-vs-fallas-menores.jpg|400]]
*Una sola P0 pesa tanto en la experiencia como muchas fallas menores.*

Cada una de las [[📏 Heurísticas de calidad de agentes]] apunta a uno de estos niveles. Ver también [[💥 Fallas de sistema frente a fallas de intención]] y [[🚑 Triage de respuestas de un agente]].

> ⚠️ Ojo de examen: **P0 = sistema** (caída, timeout, alucinación peligrosa) · **P1 = intención no cumplida** · **P2 = valor limitado** (verboso, poco útil). Las que se escapan al QA son **P1 y P2**.

## 🔁 Repaso #flashcards
¿Qué es una falla P0 en un agente?::Red Alert / System Failure: se cae, hace timeout o da una alucinación sin sentido y peligrosa.
¿Qué es una falla P1?::Missed the Mark / User Intent Not Met: funciona pero no se alinea con el objetivo del usuario.
¿Qué es una falla P2?::Usable, Not Lovable / Limited User Value: correcta pero de baja calidad, verbosa o deja trabajo al usuario.
¿Qué niveles de falla suelen escaparse del QA técnico?::P1 y P2; las P0 se suelen atrapar en QA.
