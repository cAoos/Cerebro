---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 💥 Fallas de sistema frente a fallas de intención

Una experiencia con agentes puede fallar de dos formas:

| | ⚙️ **Falla de sistema** | 🎯 **Falla de intención** |
|---|---|---|
| Qué es | Algo técnico se rompe: **código** que falla, **UI** que no funciona | El agente **técnicamente sigue sus instrucciones**, pero **no resuelve el problema del usuario** |
| Por qué importa | Fácil de detectar | **Crucial para el diseñador**: el agente funciona "como se diseñó" pero no entrega el resultado que el usuario necesita |

Salesforce clasifica las fallas de comportamiento en **tres niveles de severidad: P0, P1 y P2** (P0 = la más grave, la que **daña la confianza**). Con objetivos claros, principios probados y evaluando al agente por **cómo sirve al usuario**, se pueden **prevenir las P0**. El detalle está en [[🚨 Niveles de falla de un agente]] y [[📏 Heurísticas de calidad de agentes]].

Ver [[🎭 Diseño del comportamiento de un agente]] y [[💎 Comportamiento confiable de un agente]].

> ⚠️ Ojo de examen: si el agente **hace lo que dicen sus instrucciones pero el usuario no logra su objetivo**, es una **falla de intención**, no de sistema. **P0** es la severidad más alta.

## 🔁 Repaso #flashcards
¿Qué es una falla de sistema en un agente?::Un fallo técnico: código que se rompe o elementos de UI que no funcionan.
¿Qué es una falla de intención?::Cuando el agente sigue técnicamente sus instrucciones pero no resuelve el problema del usuario.
¿En qué niveles clasifica Salesforce las fallas de comportamiento?::P0, P1 y P2; P0 es la más grave.
