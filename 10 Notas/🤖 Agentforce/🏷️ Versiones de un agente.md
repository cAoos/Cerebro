---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 🏷️ Versiones de un agente

El ciclo de vida de las versiones de un agente en [[🏗️ Agentforce Builder]]:

```text
✏️ Draft ──💾 Save──► ✏️ Draft (editable, no está en vivo)
   │
   └──🔒 Commit Version──► 📸 Versión bloqueada ──▶️ Activate──► 🟢 En vivo
                                   │
                                   └──► nuevo Draft para seguir cambiando
```

![[builder-save-commit.jpg]]

| Estado | Qué significa |
|--------|---------------|
| ✏️ **Draft** | Editable; **Save** guarda cambios las veces que quieras, pero **no está en vivo** |
| 🔒 **Committed** | **Commit Version** guarda una **foto final** de la metadata y la **bloquea** |
| 🟢 **Active** | Se activa una versión committed para que la usen clientes o empleados |

- ☝️ **Solo una versión puede estar en vivo**: activar una nueva **apaga automáticamente** la anterior.
- 🔁 ¿Cambios a una versión committed? Se guarda como **nuevo draft**.

> ⚠️ Ojo de examen: **no se puede activar un draft**: primero hay que hacer **Commit Version**. Y no pueden convivir **dos versiones activas** del mismo agente.

> 🏋️ Ejemplo: tras personalizar Sales Coach se hace **Commit Version** y luego **Activate** ([[🛠️ Personalizar el role-play de Sales Coach paso a paso]]).

## 🔁 Repaso #flashcards
¿Cuál es el ciclo de versiones de un agente?::Draft (Save) → Commit Version (foto bloqueada) → Activate (en vivo).
¿Qué hace Commit Version?::Guarda una foto final de la metadata del agente y la bloquea para poder activarla.
¿Cuántas versiones de un agente pueden estar activas?::Solo una; activar otra apaga la anterior.
¿Cómo se modifica una versión ya committed?::Guardándola como un nuevo draft.
