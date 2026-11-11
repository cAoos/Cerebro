---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-23
---
# ✅ Validar los resultados de la IA

La IA suena **muy segura incluso cuando se equivoca**, y con agentes autónomos un error se multiplica en todo el flujo. La responsabilidad del resultado final **es siempre humana**.

## 🎚️ Cuánta supervisión
| Tipo de trabajo | La IA | La persona |
|-----------------|-------|------------|
| 🤖 **Dirigido por IA** | Tareas simples y repetitivas con reglas | Define metas, pone **guardrails**, monitorea |
| 🤝 **Apoyado por IA** | Acelera la investigación, la redacción y las ideas | Revisa, refina y verifica |
| 🧑‍⚖️ **Decisión humana** | Sintetiza datos para informar | Decide con criterio, valores y responsabilidad |

## 🔍 Revisión antes de confiar
| Revisar | Ejemplo de error |
|---------|------------------|
| 📅 **Datos correctos** | "Garantía de por vida" cuando es de 2 años |
| 🧭 **Contexto que falta** | Un correo que ignora un festivo regional |
| 🎲 **Suposiciones ocultas** | Un plan que asume semana de 5 días cuando el equipo trabaja 4 |
| ⚖️ **Sesgo** | Una estrategia pensada solo para Norteamérica |

## 🛠️ Si el resultado falla, mejora lo que le das (no solo el prompt)
- 📎 **Datos de grounding:** reportes y notas reales que anclen la respuesta.
- 🗂️ **Orden:** viñetas y encabezados.
- 📄 **Plantilla de salida:** un ejemplo de cómo debe quedar.

> ⚠️ Ojo de examen: un **modelo general** aprende de internet y tiene más sesgo; un **modelo con grounding** usa los datos de la empresa, pero se equivoca si esos datos están incompletos. Es la idea detrás de RAG ([[🗂️ Datos estructurados, semiestructurados y no estructurados]]).

Parte de la [[🌉 Fluidez en IA]].

## 🔁 Repaso #flashcards
¿Qué cuatro cosas se revisan en un resultado de IA?::Datos correctos, contexto que falta, suposiciones ocultas y sesgo.
¿Diferencia entre un modelo general y uno con grounding?::El general aprende de internet (más sesgo); el de grounding usa datos de la empresa, pero falla si esos datos están incompletos.
