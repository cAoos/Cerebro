---
tipo: nota
tema: trust-layer
estado: nueva
debil: true
fuente: "[[2026-10 Agentforce Specialist]]"
creada: 2026-11-09
---
# 🛡️ Trust Layer para el examen

Guía de repaso de todo lo que el examen pregunta sobre la Einstein Trust Layer. El concepto base está en [[🛡️ Einstein Trust Layer]]; cada pieza tiene su nota atómica.

## 🔄 El recorrido en un minuto
```text
ANTES del LLM                                   DESPUÉS del LLM
🔐 Recuperación segura (permisos/FLS)           ☣️ Detección de toxicidad (puntúa)
📥 Grounding dinámico                           🎭 Desenmascarado
🎭 Enmascarado (no en agentes)                  📜 Audit trail + feedback → Data 360
🧱 Defensa del prompt (injection/jailbreak)
            └──► 🚪 LLM Gateway ──► 🚫 Zero data retention ──┘
```

| Pieza | Una línea | Nota |
|---|---|---|
| Recuperación segura | Trae solo lo que **el usuario** puede ver | [[🔐 Recuperación segura de datos]] |
| Grounding dinámico | Mete datos del CRM o de Data 360 en el prompt | [[📥 Grounding dinámico]] |
| Enmascarado | PII → marcadores; **desactivado en agentes** | [[🎭 Enmascarado de datos]] |
| Defensa del prompt | Barandillas contra **prompt injection y jailbreak** | [[🧱 Defensa del prompt]] |
| Zero data retention | El proveedor **no guarda ni entrena** | [[🚫 Zero data retention]] |
| Toxicidad | Puntúa la respuesta por categorías dañinas | [[☣️ Detección de toxicidad]] |
| Audit trail y feedback | Todo queda en **Data 360** | [[📜 Audit trail y feedback]] |

## 🔛 Activación: el orden importa
1. **Data 360 aprovisionado** si quieres audit trail y feedback.
2. **Einstein Setup → Turn on Einstein** (IA generativa). **Hasta que no lo haces, la página de la Trust Layer no aparece en Setup.**
3. **Einstein Trust Layer** en Setup → enmascarado por modelo y patrones.
4. **Einstein Audit, Analytics, and Monitoring Setup** → activar audit y feedback y elegir el data space.
5. Permisos: *Prompt Template Manager* para crear plantillas y *Prompt Template User* para usarlas. Para ver modelos en Model Builder (Einstein Studio) hace falta un permiso de Data 360 (*Data Cloud Admin*).

## 🎯 Si la pregunta dice… → responde
| La pregunta dice… | Respuesta |
|---|---|
| "No veo la Trust Layer en Setup" | **Turn on Einstein (Generative AI)**, no "turn on Copilot" ni "turn on Prompt Builder" |
| "Reportar sobre audit y feedback" | Requiere **Data 360** |
| "Qué prompt se envió, cómo se enmascaró y la respuesta" | **Audit trail** de la Trust Layer |
| "Validar qué campos se enmascaran" | Revisar el **audit data** |
| "Modifiqué los campos enmascarados, ¿siguiente paso?" | **Probar la calidad** de las respuestas |
| "Confirmar que la toxicidad se maneja" | **Reporte del audit trail en Data 360** filtrado por detector de toxicidad |
| "Minimizar jailbreak o prompt injection" | **Prompt Defense** |
| "Que el proveedor no guarde ni entrene con mis datos" | **Zero data retention** |
| "Placeholders o datos faltantes para un usuario" | Le falta **FLS** o permisos |
| "El resumen sale pobre o incorrecto" | **Grounding incompleto o incorrecto**, no la Trust Layer |
| "El agente no enmascara PII" | **El enmascarado no aplica a agentes**: protege con permisos y acciones |

## 👁️ Vista previa de una plantilla: Resolution vs Response
Al hacer *Preview* en Prompt Builder ves dos paneles:
- **Resolution (Resolved Prompt):** el prompt **con los merge fields ya resueltos** con datos del registro de ejemplo, que es lo que se manda a la Trust Layer y al LLM.
- **Response:** lo que **generó el LLM**.

Ver [[👁️ Vista previa de una plantilla]].

> ⚠️ Ojo de examen: hay bancos viejos que marcan "Resolution = respuesta del LLM". Según la documentación de Prompt Builder, **Resolution es el prompt resuelto** y **Response es la salida**. Si te sale, razona con los nombres: *resolved prompt* frente a *response*.

## 🪤 Distractores típicos (casi siempre falsos)
- ❌ "Apagar y prender la Trust Layer" después de un cambio.
- ❌ "Toxicity Detection log en Setup" o "exportar el audit trail desde Setup".
- ❌ Debug logs, Platform Debug Logs o Flow Debugger para ver el enmascarado.
- ❌ Shield Event Monitoring o CRM Analytics para ver los prompts.
- ❌ Guardar el audit en objetos custom o big objects.
- ❌ Pedirle al LLM, con otro prompt, que te diga el dato enmascarado.

## 🔤 Nombres viejos → actuales en este tema
| Banco viejo | Hoy |
|---|---|
| Data Cloud | **Data 360** |
| Einstein Copilot Analytics | **Agentforce Analytics / Observability** |
| Página Einstein Feedback | **Einstein Audit, Analytics, and Monitoring Setup** |
| Einstein Studio | **Model Builder** (dentro de Agentforce Studio) |
| AI Specialist | **Agentforce Specialist** |

## 🧭 Gobierno más allá de la Trust Layer
El objetivo *Governance and Observability* (10 %) también cubre:
- [[🔑 Mínimo privilegio en agentes]] y [[🛂 Accesos en un proyecto de Agentforce]]: el agent user y los permission sets.
- [[🏛️ Guardrails de plataforma y de Agentforce]] y [[🚧 Guardrails para agentes autónomos]].
- [[📈 Agentforce Observability]]: analytics, session tracing y optimización.

## 🧪 Ejemplo
Cumplimiento de un banco pide tres cosas:
1. Que OpenAI no se quede con los datos → **zero data retention**.
2. Ver qué salió al modelo → **audit trail en Data 360**, que tiene que estar aprovisionado y con la recolección activada.
3. Que nadie consiga que el agente revele datos con "ignora tus instrucciones" → **Prompt Defense**, más un agent user con mínimo privilegio, porque el enmascarado **no** cubre a los agentes.

## 🔁 Repaso #flashcards
No aparece la Einstein Trust Layer en Setup, ¿qué falta?::Activar Einstein (IA generativa) en Einstein Setup.
¿Qué hace falta para reportar sobre el audit y feedback de la IA generativa?::Tener Data 360 aprovisionado y activar la recolección de audit y feedback.
¿Qué componente de la Trust Layer minimiza jailbreak y prompt injection?::Prompt Defense (defensa del prompt / system policies).
En la vista previa de Prompt Builder, ¿qué muestra Resolution?::El prompt resuelto: la plantilla con los merge fields llenos con datos del registro de ejemplo.
En la vista previa de Prompt Builder, ¿qué muestra Response?::La respuesta generada por el LLM.
¿Cómo confirmar que la toxicidad se maneja bien?::Con un reporte del audit trail en Data 360, filtrando por el tipo de detector de toxicidad.
¿Qué hacer tras cambiar los campos enmascarados?::Probar que las respuestas con datos enmascarados mantienen su calidad.
Un resumen generado sale incompleto o incorrecto: ¿causa más probable?::Datos de grounding incorrectos o incompletos.
¿Qué controles de la Trust Layer actúan antes del LLM?::Recuperación segura, grounding dinámico, enmascarado y defensa del prompt.
¿Qué controles de la Trust Layer actúan después del LLM?::Detección de toxicidad, desenmascarado y audit trail/feedback.
¿Qué permisos se necesitan para crear y para usar plantillas de prompt?::Prompt Template Manager para crear; Prompt Template User para ejecutar.
Data scientist que gestiona modelos en Model Builder y crea plantillas: ¿qué permisos?::Data Cloud Admin (Data 360) y Prompt Template Manager.
¿Qué herramienta usas para ver qué prompt salió al LLM, cómo se enmascaró y qué respondió?::El audit trail de la Einstein Trust Layer, almacenado en Data 360.
¿Qué herramienta usas para ver la adopción y el uso de un agente (sesiones, topics, acciones)?::Agentforce Analytics, en la sección Observe de Agentforce Studio.
¿Qué herramienta usas para encontrar conversaciones sin resolver y vacíos de conocimiento?::Agentforce Optimization (intents, quality scores, análisis de sesiones y tendencias).
¿Qué herramienta usas para seguir paso a paso lo que hizo un agente en una sesión (razonamiento, acciones, llamadas al LLM)?::Session Tracing, cuyos datos se guardan en Data 360.
¿Qué herramienta usas para probar cientos de frases contra un agente antes de desplegarlo?::Agentforce Testing Center (pruebas en lote con subagente, acciones y resultado esperados).
¿Qué herramienta usas para depurar una sola conversación mientras construyes el agente?::El panel de Preview / conversación de prueba del Builder, que muestra el plan, el subagente elegido y las entradas y salidas de cada acción.
¿Qué tienen en común el audit trail, Session Tracing y algunas herramientas de Observability?::Todos guardan sus datos en Data 360, que debe estar aprovisionado.
¿Sirven los debug logs o Event Monitoring para ver los prompts enviados al LLM?::No; para eso está el audit trail de la Trust Layer en Data 360. Los debug logs sirven para el Apex de una acción.
¿Cómo se ven los reportes de audit y feedback de la IA generativa?::Instalando el paquete de reportes/dashboard de Einstein Generative AI Audit and Feedback, o consultando los DMOs con el Query Editor de Data 360.
¿Qué paso de configuración hace falta antes de tener datos de audit y feedback?::Aprovisionar Data 360, activar Einstein y activar la recolección de audit y feedback eligiendo el data space.
¿Cuánto tarda en llegar el audit data a Data 360?::Hasta 24 horas.
¿Qué captura el feedback de la IA generativa?::Los pulgares arriba o abajo y comentarios de los usuarios sobre las respuestas, ligados a cada generación.
Nombre viejo "Einstein Copilot Analytics": ¿cómo se llama hoy?::Agentforce Analytics (parte de Agentforce Observability).
Un agente en producción responde peor desde ayer: ¿por dónde empiezas a investigar?::Observability: Agentforce Analytics/Optimization para ver qué sesiones fallan y Session Tracing para ver el paso exacto; luego corriges en el Builder y validas con Testing Center.
¿Dónde se ven los puntajes de toxicidad de las respuestas?::En el audit trail en Data 360, filtrando por el tipo de detector de toxicidad.
¿Qué evalúa un LLM como juez en Testing Center?::Si la respuesta real cumple el resultado esperado por significado, no por texto exacto.
Antes del LLM, ¿qué hace la Trust Layer en orden?::Recuperación segura (permisos/FLS), grounding dinámico, enmascarado y defensa del prompt; luego el LLM Gateway con zero data retention.
Después del LLM, ¿qué hace la Trust Layer?::Detección de toxicidad, desenmascarado y registro en el audit trail con el feedback.
