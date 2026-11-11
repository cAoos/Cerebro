---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 🚑 Triage de respuestas de un agente

Un agente puede **responder y aun así fallar**: prompts débiles, datos faltantes o intención poco clara dan respuestas que **suenan razonables pero no ayudan**. Con las [[📏 Heurísticas de calidad de agentes|heurísticas]] y el [[🚨 Niveles de falla de un agente|mapeo de severidad]], el diseñador prioriza dónde intervenir. Es un **ciclo continuo** de evaluar y refinar, que mantiene la **ground truth** del agente (que se comporte según la definición de "bueno" del diseñador). Los **logs del agente** son la materia prima.

**Dos ideas centrales:**
1. Toda evaluación **empieza y fluye desde la intención del usuario**.
2. Prioriza la **severidad** de las fallas, **no solo la tasa** de fallas.

## 1️⃣ Reglas para puntuar
- **Empieza por el objetivo del usuario**.
- **Basado en evidencia**: cita turnos de la conversación, no adivines.
- **Fallas en cascada**: una falla raíz arrastra otras.
- **Busca contradicciones** (pasar Approachable pero fallar Factual).
- **Ser cortés no es pasar**: lo que cuenta es el valor de la tarea.
- **Consistencia** en los estándares entre heurísticas.
- Todo **Pass / Fail / N/A lleva razón**: número de turno, comportamiento observado e impacto.
- **Un éxito temprano no excusa una falla posterior**: si pasa en el turno 1 y falla la misma heurística en el turno 5, es **fail**.
- En los pass, explica **qué salió bien**; en los fail, **qué debió hacer** y cómo afectó al usuario.

## 2️⃣ Entender el contexto
- ¿Qué quería lograr el usuario?
- ¿Qué entregó el agente?
- ¿Logró su objetivo? (**Sí / Parcialmente / No**)
- ¿Dónde se perdió el valor? (turnos y resultado)

## 3️⃣ Puntuar cada heurística y sacar la nota final
Cada heurística: **Pass, Fail o N/A**. La nota final **no es un promedio**: se asigna por el **nivel más grave observado**, porque una sola falla grave arruina la experiencia.

| Resultado | Nota final |
|---|---|
| Alguna heurística falló en nivel P0 | 🔴 **P0 Critical System Failure** |
| Sin P0, pero alguna falló en P1 | 🟠 **P1 User Intent Not Met** |
| Sin P0 ni P1, pero alguna falló en P2 | 🟡 **P2 Limited Value** |
| Todas pasan | ✅ **Pass** |

## 4️⃣ Documentar
- Heurística(s) principales que definen la nota
- **Falla raíz** (lo primero que salió mal)
- Fallas en cascada
- Impacto en el usuario (valor perdido)
- Acciones correctivas

> ⚠️ Ojo de examen: la nota de la conversación = **el nivel más grave**, **nunca un promedio**. **Ser cortés no cuenta como pass**. Un fail en el turno 5 **no se compensa** con un pass en el turno 1. Se prioriza por **severidad, no por tasa** de fallas.

## 🔁 Repaso #flashcards
¿Cómo se asigna la nota final de una conversación evaluada con heurísticas?::Por el nivel de severidad más grave observado, no por promedio.
Una conversación no tiene fallas P0 pero sí una P1 y varias P2. ¿Qué nota recibe?::P1 User Intent Not Met.
¿Qué se prioriza al evaluar agentes: la tasa de fallas o la severidad?::La severidad de las fallas.
¿Desde dónde parte toda evaluación de un agente?::Desde la intención del usuario.
El agente pasa una heurística en el turno 1 y la falla en el turno 5. ¿Resultado?::Fail; los éxitos tempranos no excusan fallas posteriores.
¿Qué valores puede tomar cada heurística al puntuar?::Pass, Fail o N/A, siempre con razón (turno, comportamiento observado e impacto).
¿Qué se documenta al cerrar una evaluación?::Heurísticas que definen la nota, falla raíz, fallas en cascada, impacto en el usuario y acciones correctivas.
