---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-06
---
# 🚀 Estrategia de despliegue de un agente

**Desplegar** = conectar el agente (que vive **dentro** de Salesforce) con el **canal** donde están los clientes: chat web, teléfono, help center… Es el **puente** entre un gran agente y una gran experiencia.

![[despliegue-adlc.jpg|500]]

En este módulo el ciclo de vida es **Plan → Build → Test → Deploy → Observe** (ver [[🔁 Ciclo de vida de un agente (ADLC)]]).

## 🪜 El proceso de despliegue
1. Crear la **estrategia de despliegue**.
2. Configurar las **conexiones** del agente **en un sandbox**.
3. Hacer **pruebas de punta a punta**.
4. **Desplegar a staging o producción** (ver [[📦 Mover un agente a producción]]).

## 🗺️ La estrategia
Es la **hoja de ruta** para maximizar el éxito del agente y **minimizar la disrupción**: anticipa problemas, maneja expectativas y recoge feedback. Conviene **armarla mientras se planea y prototipa** el agente, no al final. Un Service Agent habla directo con clientes: un lanzamiento apurado tiene consecuencias reales.

### 🧪 Rollout plan
Empezar con un **programa piloto**: un **grupo pequeño y controlado** (un equipo o un departamento). Se prueba en el mundo real **sin arriesgar a toda la empresa**, se refina y luego se **expande gradualmente**.

### 🔄 Change management y gobernanza
Factores que afectan la adopción:
- Madurez en IA y **preparación** de la organización
- **Rediseño de procesos** e integración en el flujo de trabajo
- **Gobernanza ética** de IA (ver [[⚖️ Gobernanza de IA]])
- Plan de **capacitación**, recursos y documentación
- Estrategia de **comunicación**
- **Patrocinio ejecutivo** y evangelización
- Cultura de **experimentación**, aprendizaje continuo y transparencia
- Canales de **feedback** y colaboración
- **Incentivos y reconocimiento** por adoptar IA

Siguiente paso: [[🔌 Conexiones y canales de un agente]].

> ⚠️ Ojo de examen: el rollout de un agente **arranca con un piloto** pequeño y controlado, no con toda la empresa. Las conexiones se configuran **primero en un sandbox**. La estrategia se arma **durante la planeación**.

## 🔁 Repaso #flashcards
¿Qué significa desplegar un agente?::Conectarlo a los canales donde los usuarios interactúan con él (chat web, teléfono, help center…).
¿Cuáles son los 4 pasos del proceso de despliegue de un agente?::Crear la estrategia, configurar las conexiones en sandbox, probar de punta a punta y desplegar a staging o producción.
¿Cómo se recomienda empezar el rollout de un agente?::Con un programa piloto: un grupo pequeño y controlado, y luego expandir gradualmente.
¿Cuándo conviene crear la estrategia de despliegue?::Mientras se planea y prototipa el agente.
Menciona 3 factores de change management para adoptar un agente.::Por ejemplo: patrocinio ejecutivo, plan de capacitación y canales de feedback (también comunicación, gobernanza ética, incentivos, cultura de experimentación).
