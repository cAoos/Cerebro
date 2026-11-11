---
tipo: nota
tema: trust-layer
estado: nueva
debil: false
fuente: "[[2026-10 Agentforce Specialist]]"
creada: 2026-11-09
---
# 🚫 Zero data retention

Salesforce tiene acuerdos con los proveedores de LLM externos (OpenAI, Azure OpenAI, Anthropic, Google…) para que **no guarden** los prompts ni las respuestas y **no entrenen** sus modelos con ellos. El dato se procesa y se olvida.

- 🏠 Los modelos **alojados por Salesforce** (dentro de su perímetro de confianza) ya cumplen esto por diseño.
- 🔌 Con **Bring Your Own LLM** (Model Builder) **tu** contrato con el proveedor define la retención: el acuerdo de Salesforce no te cubre. Ver [[🔌 Opciones de LLM en Salesforce]].
- 🚪 Todo pasa por el **LLM Gateway**, que es la puerta única hacia los modelos.

## 🧪 Ejemplo
Un banco pregunta si OpenAI va a entrenar con los datos de sus clientes al usar Agentforce. No: con los modelos gestionados por Salesforce aplica zero data retention. Si el banco conecta su propio modelo con BYOLLM, depende de su contrato con ese proveedor.

> ⚠️ Ojo de examen: "¿Qué garantiza que el proveedor no guarde ni entrene con los datos?" → **zero data retention**. No es el enmascarado: el enmascarado oculta los datos, pero no es un acuerdo de retención.

Parte de [[🛡️ Einstein Trust Layer]] · Guía: [[🛡️ Trust Layer para el examen]]

## 🔁 Repaso #flashcards
¿Qué es zero data retention?::El acuerdo con los proveedores de LLM externos para que no guarden prompts ni respuestas y no entrenen con ellos.
¿Aplica el zero data retention de Salesforce a un modelo propio conectado con BYOLLM?::No automáticamente; la retención depende del contrato del cliente con ese proveedor.
