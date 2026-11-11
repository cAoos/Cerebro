---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-05
---
# 🌡️ Temperatura y modelos custom

La **temperatura** de un [[🧠 Modelos de lenguaje grandes (LLM)|LLM]] controla **qué tan aleatorias** son sus respuestas:

| Temperatura | Comportamiento | Para qué |
|---|---|---|
| 🧊 **Baja (cerca de 0)** | **Determinista, enfocada, predecible**, algo repetitiva | Escritura de negocio, menos alucinación |
| 🔥 **Alta (cerca de 1)** | **Aleatoria, creativa, diversa**, menos predecible | Lluvia de ideas, textos creativos |

## 🧰 Crear un modelo custom (AI Models editor)
En Prompt Builder: **Template Settings → Model → Details →** ícono **Manage Model**. Se abre el **AI Models editor**:
1. **Edit → Create model**.
2. Mover el slider de **Temperature**, por ejemplo a **0.3**. Se puede probar con un prompt de muestra y **Generate** antes de guardar.
3. **Save →** nombre (*Business Writing*) y descripción (*"less creative, and therefore should hallucinate less"*) **→ Create Model**.

![[modelo-temperatura.jpg|400]]

## 🔀 Usarlo en una plantilla
En **Template Settings → Model**:
- **Model Type = Standard**: modelos de fábrica (p. ej. OpenAI GPT 4 Omni Mini).
- **Model Type = Custom**: los modelos que creaste (p. ej. Business Writing).

![[modelo-standard.jpg|300]]
![[modelo-custom.jpg|300]]

Con el modelo controlas **tono y estilo, punto de vista y consideraciones éticas** de la respuesta. Ver también [[🎚️ Principios para elegir un modelo]].

> ⚠️ Ojo de examen: si piden respuestas **más predecibles** o **menos alucinaciones**, **baja la temperatura**. Si piden más **creatividad o variedad**, súbela. Un modelo con parámetros propios se crea en el **AI Models editor** y se elige en la plantilla con **Model Type = Custom**.

## 🔁 Repaso #flashcards
¿Qué controla la temperatura de un LLM?::La aleatoriedad de las respuestas: baja = predecible y enfocada; alta = creativa y diversa.
Leadership quiere respuestas más predecibles y con menos alucinación. ¿Qué ajustas?::Bajar la temperatura del modelo (por ejemplo a 0.3) en un modelo custom.
¿Dónde se crea un modelo con temperatura personalizada?::En el AI Models editor (desde Prompt Builder → Template Settings → Model → Details → Manage Model).
¿Cómo se elige un modelo custom en una plantilla?::En Template Settings, con Model Type = Custom y el modelo en el dropdown.
