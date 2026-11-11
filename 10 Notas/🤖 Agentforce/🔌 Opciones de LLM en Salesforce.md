---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-23
---
# 🔌 Opciones de LLM en Salesforce

| Opción | Qué es | Dónde corre |
|--------|--------|-------------|
| ☁️ **Gestionados por Salesforce** | Modelos habilitados por defecto, listos para usar desde **Prompt Builder** o la **Models API** | LLM en internet, a través de la Trust Layer |
| 🏠 **De terceros alojados en Salesforce** | Modelos de **Amazon, Anthropic, Cohere** y otros, alojados dentro de Salesforce | **Infraestructura de Salesforce**: las solicitudes y respuestas no salen |
| 🧳 **BYOLLM** (*Bring Your Own LLM*) | Conectas tu propio modelo, entrenado fuera, para usarlo con **plantillas personalizadas de Prompt Builder** | Tu infraestructura, pero igual pasa por la **pasarela del LLM y la Trust Layer** |

> ⚠️ Ojo de examen: por defecto, el **motor de razonamiento de Agentforce usa GPT-4o** (de OpenAI o Azure OpenAI). Se puede elegir otro modelo.

**Cómo elegir un modelo** 🎚️: capacidades · costo · calidad de las respuestas · velocidad. Muchas empresas usan **varios LLM**, uno por caso de uso (código, opiniones, contenido). Ver [[🎚️ Principios para elegir un modelo]].

🌍 **Modelos según la zona geográfica:** envían la solicitud al centro de datos donde está aprovisionado Data 360. Así hay más control sobre la residencia de los datos y menos latencia.

Todas las opciones pasan por la [[🛡️ Einstein Trust Layer]].

![[llm-opciones-salesforce.jpg]]

## 🚦 Controlar qué modelos se usan
El objetivo oficial pide *gestionar e impedir el acceso a modelos específicos*. Lo confirmado:
- 🧪 Los modelos se administran en **Model Builder** (AI Models, antes Einstein Studio): ahí se agregan los **BYOLLM** y se crean **configured models**. Una plantilla **solo puede elegir los modelos disponibles** en la org.
- 🔐 El acceso a usar IA se controla con **permission sets** (Prompt Template Manager y User) y con la **configuración de Einstein** en Setup.
- 🧯 Un modelo propio que no debe usarse se puede **quitar o no conectar**, y un **modelo de terceros alojado en Salesforce** evita que los datos salgan de su infraestructura.
- ⚙️ Hay un ajuste para **habilitar o no los modelos beta** (`enableAIModelBeta`, apagado por defecto).

> ⚠️ Por confirmar: no encontré la doc oficial de un interruptor para **deshabilitar un modelo concreto** de Salesforce. Si sale en el examen, piensa en **Model Builder** (dónde se gestionan) y en **permisos** (quién accede).

## 🔁 Repaso #flashcards
¿Cuáles son las tres opciones de LLM en Salesforce?::Gestionados por Salesforce, de terceros alojados en Salesforce, y BYOLLM.
¿Qué modelo usa por defecto el motor de razonamiento de Agentforce?::GPT-4o (OpenAI o Azure OpenAI).
¿Con qué se usa un modelo BYOLLM?::Con plantillas personalizadas de Prompt Builder, y pasa por la Trust Layer.
