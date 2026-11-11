---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-09
---
# 🏭 Agentforce for Industries

Agentforce aplicado a las **Industry Clouds** de Salesforce: Financial Services, Health & Life Sciences, Nonprofit, Manufacturing, Public Sector, Retail… Son más de una docena de soluciones de industria. Lo que cambia frente a un agente genérico es que **ya trae el contexto de la industria**.

## 🧰 Qué aporta la industria al agente
| Pieza | Qué le da al agente |
|---|---|
| 👤 **Roles ya definidos** en la Industry Cloud | Sabe para quién trabaja: gift officer, asesor financiero, profesional de salud… |
| 🗃️ **Modelo de datos de la industria** | Un **grounding** más rico, y por eso respuestas más **precisas** |
| 📚 **Biblioteca de procesos de dominio** | Unos 10 años de procesos de negocio que se usan como **acciones de Agentforce listas de fábrica** |
| 🛡️ **Funciones de cumplimiento** | **Refuerzan la Trust Layer** en industrias reguladas (por ejemplo, privacidad de datos de salud) |

- 🧱 Los bloques básicos no cambian: **topics, actions e instructions**.
- 🔧 La recomendación es **extender** los prompts y acciones de fábrica con procesos propios o con una conexión a **Data 360**.
- 🎯 La primera decisión al diseñar el agente sigue siendo el **caso de uso y los objetivos de negocio** (ver [[🗒️ Planear un agente]]).

## 🎯 Problemas que resuelve
- Empleados que gastan tiempo en tareas **repetitivas o de poco valor**.
- **Demasiadas tareas** y poca gente para hacerlas.
- Interacciones **fluidas**, tanto cuando el cliente escribe como cuando la empresa sale a buscarlo.
- **Lealtad y confianza** a partir de interacciones personalizadas.

## 🧪 Ejemplo
Una aseguradora en Financial Services Cloud no construye desde cero el proceso de "consultar el estado de una póliza": usa la acción que ya trae la industria. El agente se apoya en el modelo de datos de pólizas y siniestros para responder bien, y escala al asesor humano cuando la petición sale de sus guardrails.

> ⚠️ Ojo de examen: si preguntan por qué un agente de una Industry Cloud es **más preciso**, la respuesta es que el **modelo de datos de la industria da mejor grounding**. Si preguntan cómo arrancar más rápido, son las **acciones de fábrica** de la biblioteca de procesos de dominio. En industrias reguladas, el cumplimiento **complementa** la [[🛡️ Einstein Trust Layer]]; no la reemplaza.

Casos por industria: [[🏦 Casos de uso de Agentforce por industria]] · Banca: [[💳 Agentforce for Financial Services]] · Ver también [[🏥 Headless en salud]] · [[💰 Headless en servicios financieros]]

## 🔁 Repaso #flashcards
¿Qué hace más preciso a un agente construido sobre una Industry Cloud?::El modelo de datos de la industria, que da un grounding más rico.
¿Qué son las acciones de fábrica de Agentforce for Industries?::Procesos de negocio específicos del dominio, acumulados por años en las Industry Clouds, que se usan como acciones de Agentforce listas para usar.
¿Cómo ayudan las funciones de cumplimiento de industria a la Trust Layer?::La refuerzan en entornos regulados (p. ej. guardrails de privacidad de datos de salud); no la reemplazan.
¿Cuáles son los bloques básicos de un agente, también en industrias?::Topics, actions e instructions.
¿Cuál es la primera decisión al diseñar un agente de industria?::Definir el caso de uso y los objetivos de negocio.
