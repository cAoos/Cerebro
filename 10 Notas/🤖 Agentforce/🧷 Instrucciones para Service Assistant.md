---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-08
---
# 🧷 Instrucciones para Service Assistant

En Service Assistant, el **subagente es una categoría** para un tipo de caso, y sus **instrucciones** contienen los detalles para resolverlo. Con la info del caso, el agente **clasifica** el caso en un subagente y elige las instrucciones relevantes para el **service plan**. Concepto en [[🪄 Agentforce Service Assistant]].

| Guía | Ejemplo | Por qué |
|---|---|---|
| 🔀 **Condicionales** | *"If vaccinations are required…, provide a link…"* | Cubrir **todos los escenarios** del tipo de caso |
| 📜 **Políticas de la empresa** | *"Documents must be uploaded no later than two weeks before departure"* | Ser específico: criterios, condiciones y pasos; incluir **tono**, guiones y plantillas |
| 🎯 **Resultados esperados en orden** | *"Once you confirm…"*, *"When you have…"*, *"After…"* | Lenguaje **secuencial** para que los pasos salgan en orden lógico |
| ❗ **Pasos obligatorios** | *"Always include this as a step in the plan"* | Órdenes directas para que no falte lo crítico |

En el subagente también se define una **Classification Description** con varios tipos de pregunta (para clasificar bien) y un **Scope** con límites (*"You must not provide legal advice…"*).

> ⚠️ Ojo de examen: si la información de la empresa **no está en las instrucciones, no aparece en el plan**. Una **Data Library con Knowledge** puede **llenar los huecos** y simplificar las instrucciones. Las **acciones no son necesarias**. Mismo estilo que [[📝 Instrucciones de razonamiento]] y [[🔀 Instrucciones condicionales]].

## 🔁 Repaso #flashcards
¿Qué papel cumple un subagente en Service Assistant?::Es la categoría de un tipo de caso; agrupa las instrucciones para resolverlo.
¿Qué 4 guías se recomiendan al escribir instrucciones para Service Assistant?::Usar condicionales, especificar políticas de la empresa, indicar resultados esperados en orden y usar órdenes directas para pasos obligatorios.
¿Qué lenguaje asegura el orden de los pasos del plan?::Lenguaje secuencial como "When you have…" y "After…".
¿Cómo se asegura que un paso siempre esté en el plan?::Con una orden directa como "Always include this as a step in the plan".
¿Qué pasa si una política no está en las instrucciones?::No aparecerá en el service plan, salvo que la cubra Knowledge vía Data Library.
¿Qué se incluye en las instrucciones además de los pasos?::Tono, guiones de ejemplo y plantillas disponibles para el agente de servicio.
