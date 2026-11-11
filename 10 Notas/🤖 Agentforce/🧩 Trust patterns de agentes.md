---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 🧩 Trust patterns de agentes

Los **trust patterns** son **diseños estándar de producto** que Salesforce aplica en todos sus productos para mejorar la seguridad de los agentes.

| Trust pattern | Cómo se aplica |
|---|---|
| 🎯 **Reduce hallucinations** | **Clasificación por topic**: mapea el input del usuario a un topic específico |
| 📧 **Limit the frequency of agent-generated emails** | Tope de emails para no saturar y que cada comunicación sea significativa |
| 🔕 **Respect user privacy** | Función de **opt-out** en el CRM: el usuario controla cada cuánto recibe comunicaciones de agentes |
| 🪟 **Create transparency by design** | El contenido generado por IA se **declara directa y transparentemente** |
| 🤝 **Facilitate smooth AI-human handoffs** | Transiciones suaves agente → humano: **copiar al gerente de ventas** en emails de IA o un **dashboard de supervisión humana** |

Forman parte de los [[🏛️ Guardrails de plataforma y de Agentforce]] y aterrizan los principios de [[🌟 IA agéntica confiable]].

> ⚠️ Ojo de examen: **opt-out → privacidad**; **topic classification → alucinaciones**; **copiar al sales manager / dashboard → handoff humano-IA**; **límite de emails** sobre todo aplica al **SDR**.

## 🔁 Repaso #flashcards
¿Qué son los trust patterns de Salesforce?::Diseños estándar de producto que mejoran la seguridad de los agentes.
¿Qué trust pattern usa la clasificación por topic?::Reduce hallucinations.
¿Qué trust pattern usa la función de opt-out?::Respect user privacy.
¿Cómo se facilita el handoff humano-IA según los trust patterns?::Copiando al gerente de ventas en los emails generados por IA o con un dashboard de supervisión humana.
¿Cuáles son los 5 trust patterns de agentes?::Reduce hallucinations, limit email frequency, respect user privacy, transparency by design y smooth AI-human handoffs.
