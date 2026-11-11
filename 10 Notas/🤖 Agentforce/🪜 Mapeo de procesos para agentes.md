---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-01
---
# 🪜 Mapeo de procesos para agentes

Igual que no contratas a alguien sin onboarding, **no despliegues un agente que no puede seguir tus procesos**. Si no puedes describir cómo se hace el trabajo, **es casi imposible configurar un agente** para hacerlo.

**Process mapping** = representación visual (flujograma, swimlanes…) de los pasos de un proceso de inicio a fin: cuándo empieza y termina cada paso, qué entradas y datos requiere.

![[planear-agente-mapa-proceso.jpg]]

## ❓ Preguntas para cada proceso
- 🎯 ¿Qué **objetivo** tiene el usuario y **cómo lo expresaría**?
- 🔢 ¿Qué procesos y **pasos**, en qué **orden**, cuándo empiezan y terminan?
- 📜 ¿Qué **políticas, reglas y guardrails** aplican a cada paso?
- 🔀 ¿Dónde se **toman decisiones** y cómo?
- 💬 ¿Qué **preguntas aclaratorias** haría el agente? ¿Cuándo debe el usuario **confirmar** antes de seguir?
- 🗄️ ¿Qué **datos** son obligatorios u opcionales? ¿Qué **input** con qué **formato**?
- 📤 ¿Qué **resultado** tiene cada paso y cómo se mide el éxito?
- 🗣️ ¿Cuándo usar un **lenguaje específico**? ¿Qué temas **nunca** tocar?
- 🙋 ¿Cuándo **escalar** a un humano?

Coral Cloud **no hizo diagramas formales**: respondió estas preguntas mientras prototipaba.

## 🧱 De procesos a bloques del agente
Los procesos se traducen en **[[🗂️ Subagentes|subagentes]]** (los trabajos), sus **instrucciones** y sus **[[⚡ Acciones de agente|acciones]]** (las herramientas). El agente elige el subagente más relevante y lanza sus acciones.

![[planear-agente-subagente-acciones.jpg]]

Primero revisar la **librería de acciones estándar**; si nada sirve, ir a **custom**. Siguiente: [[🧬 Diseñar un subagente]].

> ⚠️ Ojo de examen: el mapeo de procesos es la base para diseñar **subagentes, acciones e instrucciones**. Si el proceso no está bien definido, el agente no lo puede ejecutar.

## 🔁 Repaso #flashcards
¿Qué es el process mapping?::Una representación visual de los pasos de un proceso de negocio de inicio a fin, con su secuencia, entradas y datos.
¿Por qué mapear procesos antes de configurar un agente?::Porque si no puedes describir cómo se hace el trabajo, no puedes configurar un agente para hacerlo.
¿En qué se traducen los procesos mapeados dentro del agente?::En subagentes, instrucciones y acciones.
Nombra tres preguntas clave al mapear un proceso para un agente::Cómo expresa el usuario su objetivo; dónde se toman decisiones; cuándo escalar a un humano (también: qué datos, qué confirmar, qué temas evitar).
