---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 🪢 Contrato de cuatro vías

El nuevo "lienzo" del diseñador: **cuatro componentes** que deben estar alineados. **Alineados → agente de alto rendimiento. Desalineados → la experiencia se rompe.** Parte del [[🎭 Diseño del comportamiento de un agente]].

| Componente | Cambio de diseño | Métrica |
|---|---|---|
| 🌟 **Intención del usuario** (la estrella polar) | De "¿qué botón tocó?" a "**¿qué resultado quiere lograr?**" | ¿Descifra bien el lenguaje y el **subtexto** para hallar el objetivo real? |
| 🎛️ **El spec** (control de misión) | El espacio de diseño es el **system prompt**: **persona, tono y reglas de límites** | ¿Se mantiene **en marca** y sigue las políticas aunque la conversación se complique? |
| 🗄️ **Los datos** (fuente de verdad) | El diseñador **cura la base de conocimiento**; grounding en datos del CRM en tiempo real o documentación | ¿Respuestas **factuales y útiles**, o inventa? |
| 🧠 **El modelo** (motor cognitivo) | Conocer los **límites de razonamiento** del LLM para fijar expectativas realistas | ¿Tiene el razonamiento para resolver **sin escalar a un humano demasiado pronto**? |

Ver [[📥 Grounding dinámico]] y [[🧠 Modelos de lenguaje grandes (LLM)]].

> ⚠️ Ojo de examen: los cuatro son **intención, spec, datos y modelo**. Si el agente **inventa** → problema de **datos**. Si se sale de **marca o política** → problema del **spec**. Si **escala demasiado pronto** → límite del **modelo**.

## 🔁 Repaso #flashcards
¿Cuáles son los cuatro componentes del contrato de cuatro vías?::Intención del usuario, el spec (system prompt), los datos y el modelo.
¿Qué define el spec de un agente?::La persona, el tono y las reglas de límites, en el system prompt.
¿Qué mide el componente de datos?::Si el agente da respuestas factuales y útiles en vez de inventar.
¿Qué mide el componente del modelo?::Si tiene la capacidad de razonamiento para resolver sin escalar a un humano demasiado pronto.
¿Qué pasa cuando los cuatro componentes no están alineados?::La experiencia del usuario se rompe.
