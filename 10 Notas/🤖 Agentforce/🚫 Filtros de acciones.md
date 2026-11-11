---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-30
---
# 🚫 Filtros de acciones

Ocultan una [[⚡ Acciones de agente|acción]] **al LLM** cuando no se cumplen las condiciones de negocio. Si el LLM **no ve la acción, no puede usarla**: aunque el cliente intente convencerlo, el agente **físicamente no tiene acceso**. Es la forma **determinista** de hacer cumplir reglas. Ver [[🎯 Determinismo en Agentforce]].

## ➕ Cómo se agrega (Canvas)
1. Subagente → **Actions Available for Reasoning** → expandir la acción → **Add filter**.
2. **Available when:** condición sobre [[🔣 Variables de agente|variables]], combinable con **And**.
3. Opcional: **Follow-up action → Set a variable** para cambiar el estado después de ejecutarla.

![[determinismo-add-filter.jpg]]

## 🏝️ Ejemplo: un crédito por sesión
![[determinismo-accion-filtrada.jpg]]
- **Available when:** `isCreditIssued == False` **And** `LifetimeValue >= 25000`.
- **With input:** `amount`, `contactId` = **Agent Populated** (el agente los llena).
- **Set variable:** `isCreditIssued = True` → después del primer crédito la acción **desaparece**.

En Agent Script:
```
available when @variables.customerVerified == True and @variables.officeOpen == True
```
→ la acción solo existe para el LLM si **ambas** son True.

> 💡 `isCreditIssued` se reinicia por sesión: en producción habría que validar con un **flow** si ya recibió crédito en esa estadía.

> ⚠️ Ojo de examen: "¿cómo evitas que el agente ejecute X si no se cumple Y, **aunque el usuario insista**?" → **filtro de acción** (`available when`), no instrucciones en el prompt. Con varias condiciones unidas por `and`, **todas** deben cumplirse.

## 🔁 Repaso #flashcards
¿Qué hace un filtro de acción?::Oculta la acción al LLM si no se cumplen las condiciones; sin verla, no puede ejecutarla.
¿Por qué un filtro es más seguro que una instrucción de prompt?::Porque es determinista: el LLM ni siquiera ve la acción, así que no se equivoca ni lo convencen.
¿Cómo se escribe un filtro en Agent Script?::available when @variables.X == valor (combinable con and).
¿Cómo se evita que una acción se ejecute dos veces en la sesión?::Con un follow-up action que pone una variable en True y un filtro que exige que esa variable sea False.
Con "available when customerVerified == True and officeOpen == True", ¿cuándo puede el LLM usar la acción?::Solo cuando las dos variables son True.
