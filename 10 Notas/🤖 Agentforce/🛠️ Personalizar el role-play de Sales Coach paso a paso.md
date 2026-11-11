---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-08
---
# 🛠️ Personalizar el role-play de Sales Coach paso a paso

Proyecto *Build Your First Sales Coach*. El setup (wizard de 4 pasos, usuario, permisos, componente) es el mismo de [[🛠️ Configurar Agentforce Sales Coach paso a paso]]; aquí va lo **nuevo**: ajustar el comprador, sumar la acción de feedback y editar el prompt. Teoría en [[🎨 Personalizar Agentforce Sales Coach]].

## 1️⃣ Ajustar el subagente Negotiation/Role-Play
En el **Explorer** del Agentforce Builder, abrir **Negotiation/Role-Play** y reemplazar:
- **Descripción**: comprador en evaluación tras una demo; temas: huella de carbono, competencia, precio, términos del contrato.
- **Reasoning Instructions**: comprador **molesto y escéptico** que busca el mejor trato, contraoferta y se queja si no le dan **estadísticas y casos concretos**.
- Instrucción *"When asked to start the negotiation…"*: saludo fijo y **no repetirlo** si ya está en el historial.

![[coach-subagente-negociacion.jpg]]

## 2️⃣ Agregar la acción de feedback
**+** junto al subagente → **Add from Asset Library** → buscar *negotiation* → **Agentforce Sales Coach: Give Feedback on Negotiation/Review Stage** → Add to Agent → Save.

![[coach-asset-library.jpg]]

## 3️⃣ Editar el prompt de esa acción
1. Setup → **Agentforce Assets** → pestaña **Actions** → la acción → sección **Reference Action** → abrir el prompt (aviso *Can't edit prompt template* → OK).
2. **Preview Settings** → pegar una **Transcript** → elegir la oportunidad → **Preview**.
3. **Save as a New Version** → bajo **<NEGOTIATION QUESTIONS>** agregar preguntas propias (huella de carbono, descuento por lanzamiento). **No borrar la etiqueta**: el prompt la referencia en varios lugares.
4. **Save & Preview** → comparar → **Activate**.

![[coach-agentforce-assets.jpg]]
![[coach-test-inputs.jpg]]
![[coach-negotiation-questions.jpg]]

## 4️⃣ Publicar el agente
Agentforce Studio → Sales Coach Agent → **Commit Version** → **Activate** (ver [[🏷️ Versiones de un agente]]).

> ⚠️ Ojo de examen: el prompt de una acción se encuentra en **Setup > Agentforce Assets > Actions > Reference Action**. Un prompt de fábrica no se edita directo: **Save as a New Version**. Las etiquetas tipo **<NEGOTIATION QUESTIONS>** son **delimitadores** que el prompt reutiliza.

Uso del resultado: [[🎤 Practicar con Agentforce Sales Coach]].

## 🔁 Repaso #flashcards
¿Dónde se cambia la personalidad del comprador en el role-play de negociación?::En la descripción y las Reasoning Instructions del subagente Negotiation/Role-Play en el Agentforce Builder.
¿Cómo se agrega una acción existente a un subagente?::Con el + del subagente → Add from Asset Library → Select → Add to Agent.
¿Qué acción de feedback se agrega al subagente de negociación?::Agentforce Sales Coach: Give Feedback on Negotiation/Review Stage.
¿Dónde se encuentra el prompt template de una acción?::Setup > Agentforce Assets > Actions > la acción > Reference Action.
¿Por qué no se debe borrar la etiqueta <NEGOTIATION QUESTIONS>?::Porque el prompt la referencia en varios lugares; es un delimitador.
¿Qué se hace al final para publicar el Sales Coach personalizado?::Commit Version y luego Activate en Agentforce Studio.
¿Cómo se evita que el agente repita el saludo inicial?::Con una instrucción: si ya lo dijo en el historial de la conversación, no repetirlo.
