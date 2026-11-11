---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 📭 Escenario del reporte que desaparece

Ejercicio del módulo de [[🔬 Threat modeling de flujos con agentes|threat modeling]]: el **reporte trimestral de cumplimiento** aparece como **generado pero nunca llegó al regulador**, y el agente asegura que "**completó todos los pasos con éxito**".

| Paso | Quién | Qué pudo fallar | Qué lo habría evitado |
|---|---|---|---|
| 1. Recolectar datos de finanzas | 🤖 Agente | **Nunca arrancó** la recolección | **Trigger check**: confirmar que el proceso inició y la recolección terminó |
| 2. Generar el reporte | 🤖 Agente | Lo creó pero **no lo guardó** en la carpeta correcta ni lo marcó para envío | **Chequeo automático**: guardado, bien nombrado y listo para entregar |
| 3. Revisar el reporte | 🧑 Humano | Aprobó, pero **no verificó que se disparó el envío** | **Checklist o dashboard** con estado de entrega: pendiente, en progreso, completo |
| 4. Enviar por email | 🤖 Agente | El envío **falló o expiraron los permisos** y **no hubo alerta** | **Confirmación de entrega y notificación** al revisor |

**Lección:** pequeñas rupturas (un **chequeo faltante**, **dueño poco claro**, **fallas sin reportar**) se propagan aunque cada pieza parezca funcionar. Las ven primero desarrolladores, admins y ciberseguridad.

Preguntas para cualquier flujo: ¿dónde pudo **no pasar al siguiente paso**? ¿qué **control** lo habría detectado antes? ¿**a quién** había que avisar?

> ⚠️ Ojo de examen: la falla típica de un agente en un flujo **no es un error visible**, es una **falla silenciosa** entre pasos. La solución son **checks entre pasos, confirmación de entrega y alertas**.

## 🔁 Repaso #flashcards
En el escenario del reporte que desaparece, ¿qué habría detectado que el email falló?::Una confirmación de entrega con notificación al revisor.
¿Qué tres preguntas se hacen sobre cada paso del flujo en el escenario del reporte?::Dónde pudo no pasar al siguiente paso, qué control lo habría detectado antes y a quién había que avisar.
¿Qué le faltó al revisor humano en el escenario del reporte?::Verificar que se disparó el envío; un checklist o dashboard con el estado de entrega lo habría resuelto.
