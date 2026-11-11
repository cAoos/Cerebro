---
tipo: nota
tema: prompts
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-27
---
# 🧾 Tipos de plantillas de Prompt Builder

Las **Prompt Templates** permiten **reutilizar** un prompt con datos de Salesforce. Se crean en **Setup → Prompt Builder → New Prompt Template**.

| Tipo                     | Qué hace                                                                     | Patrón ([[🧭 Patrones de prompts]]) |
| ------------------------ | ---------------------------------------------------------------------------- | ----------------------------------- |
| 📧 **Sales Email**       | Borrador de correo personalizado para un cliente con datos del sistema       | ✍️ Generación                       |
| 🏷️ **Field Generation** | Completa **un campo** de un registro. Ver [[🏷️ Plantilla Field Generation]] | ✍️ Generación / 📝 Resumen          |
| 📝 **Record Summary**    | Resumen del registro                                                         | 📝 Resumen                          |
| 🧩 **Flex**              | Lo que no encaja en los otros tres. Ver [[🧩 Plantilla Flex]]                | Cualquiera                          |

![[prompt-builder-setup.png]]
![[prompt-builder-nueva-plantilla.png]]

> ⚠️ Ojo de examen: preguntas tipo "¿qué plantilla usarías para…?". Llenar un campo → **Field Generation** · correo a un contacto → **Sales Email** · necesito entradas libres de varios objetos → **Flex**.

Cómo se les dan datos: [[🔗 Grounding de plantillas]]. Cómo se prueban: [[👁️ Vista previa de una plantilla]]. Paso a paso con capturas: [[🛠️ Crear una plantilla Sales Email paso a paso]], [[🛠️ Crear una plantilla Field Generation paso a paso]] y [[🛠️ Crear una plantilla Flex paso a paso]].

> 🔲 Las plantillas también se corren **en lote, una por fila**, con la columna Prompt Template de [[🔲 Agentforce Grid]].

## 🔁 Repaso #flashcards
¿Cuáles son los cuatro tipos de plantilla de Prompt Builder?::Sales Email, Field Generation, Record Summary y Flex.
¿Qué tipo de plantilla usarías para llenar un campo de un registro con IA?::Field Generation.
