---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-30
---
# 🔀 Instrucciones condicionales

Agentforce puede mandar **prompts totalmente distintos al LLM según el valor de las [[🔣 Variables de agente|variables]]**.

🆚 En otros agentes **se manda el prompt completo en cada turno**, sin importar el contexto, y dependes de prompt engineering complicado y suerte. En Agentforce, la **lógica de razonamiento se resuelve primero** y **solo el prompt resultante** llega al LLM: siempre específico para el **estado actual** del agente.

## ➕ Cómo se agregan (Canvas)
1. En las instrucciones del subagente, escribir **`/`** → menú **Inline Actions** → **If/Else (Conditional)**.
2. Elegir variable, operador y valor (ej: `LifetimeValue >= 50000`).
3. Escribir la instrucción que va dentro del if.

![[determinismo-inline-actions.jpg]]
![[determinismo-if-else-canvas.jpg]]

Dentro del if se pueden citar acciones con **`@`** (ver [[📝 Instrucciones de razonamiento]]):

![[determinismo-if-con-accion.jpg]]

## 📜 En Agent Script
```
reasoning:
    instructions: ->
        if @variables.loyalty_tier == "Basic":
            | Si quiere devolver algo, explica que Basic no tiene devoluciones...
        if @variables.loyalty_tier == "Premium":
            | Confirma el pedido y procesa con {!@actions.create_return}.
```
`if` = lógica que resuelve Agentforce · `|` = texto que se manda al LLM. Si un cliente **Basic** pide una devolución, el LLM **solo recibe el primer texto**: nunca ve la instrucción de `create_return`.

> ⚠️ Ojo de examen: el condicional decide **qué texto llega al LLM**; lo que no cumple la condición **no se envía**. Ojo: el condicional **no oculta la acción** por sí solo, para eso están los [[🚫 Filtros de acciones]].

## 🔁 Repaso #flashcards
¿Qué ventaja tienen las instrucciones condicionales frente a mandar todo el prompt?::Agentforce resuelve la lógica primero y solo envía al LLM el prompt que aplica al estado actual.
¿Cómo se agrega un if/else en Canvas?::Escribiendo / para abrir Inline Actions y eligiendo If/Else (Conditional).
En Agent Script, ¿qué significa la línea que empieza con |?::Es el texto de la instrucción que se envía al LLM.
Si la variable no cumple ninguna condición, ¿qué recibe el LLM?::Ninguna de esas instrucciones condicionales.
¿Basta un condicional para impedir que el LLM use una acción?::No: la acción sigue disponible. Para ocultarla se usa un filtro de acción.
