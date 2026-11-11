---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-01
---
# 📞 Canales y escalamiento de un agente

Parte de los requisitos técnicos en [[🗒️ Planear un agente]], junto con datos, seguridad ([[🛂 Accesos en un proyecto de Agentforce]]) y [[☑️ Requisitos de Salesforce para Agentforce]].

## 🗄️ Datos
Auditar los datos en: completitud, calidad, comprensibilidad, cardinalidad, unicidad, accesibilidad, **recencia**, seguridad y gobierno. Ver [[📋 Requisitos de datos de un proyecto de IA]]. Herramienta gratis: **Cuneiform** en [[🏪 AgentExchange]].

## 💬 Canales
¿Cómo interactúa el agente con usuarios internos o externos? Coral Cloud empieza con **mensajería** (web, **WhatsApp**, **Facebook Messenger**) y luego teléfono y email. Usa **Enhanced Chat** en su sitio de Experience Cloud, que soporta todos esos canales. Ver [[🌐 Desplegar un Service Agent en Experience Cloud]].

💡 Puedes **prototipar sin canales**, pero la **estrategia de canales** debe estar lista **antes de producción** y hay que probar el agente **en cada canal**.

## 🙋 Escalamiento a humanos
Motivos: **política** de la empresa, requisitos de **marca**, **seguridad**, gestión de **riesgo** o **cumplimiento regulatorio**. Definir **cuándo y cómo** interviene un humano ayuda a configurar los guardrails.

🔀 **Enrutamiento**: si ya usas **Omni-Channel**, hay que integrarlo con el agente (guía *Deploy Your Agent to Channels*).

> ⚠️ Ojo de examen: **Enhanced Chat** soporta web, WhatsApp y Messenger. El enrutamiento agente → humano va por **Omni-Channel**. La estrategia de canales es obligatoria **antes de producción**, no antes del prototipo.

Cómo se asigna un escalamiento a un rep: [[🧑‍⚖️ Cómo decide Omni-Channel a quién asignar]].

## 🔁 Repaso #flashcards
¿Qué solución de chat soporta web, WhatsApp y Facebook Messenger para el agente?::Enhanced Chat.
¿Con qué se enruta una conversación del agente a un rep humano?::Con Omni-Channel, integrado con el agente.
¿Se necesita configurar canales para prototipar un agente?::No; pero la estrategia de canales debe estar lista antes de producción y probarse en cada canal.
¿Qué motivos justifican escalar a un humano?::Política de la empresa, requisitos de marca, seguridad, gestión de riesgo o cumplimiento regulatorio.
