---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 🔬 Threat modeling de flujos con agentes

**Threat modeling**: forma estructurada de ver cómo funciona un sistema, **qué puede salir mal** y cómo manejarlo **antes** de que pase.

## 🆚 STRIDE frente al nivel de flujo
- **STRIDE** = **S**poofing, **T**ampering, **R**epudiation, **I**nformation disclosure, **D**enial of service, **E**levation of privilege. Lo usan los desarrolladores para amenazas **técnicas** en aplicaciones.
- Pero **ni el mejor STRIDE** atrapa los riesgos que vienen de **cómo se usan** los agentes: **aprobaciones faltantes**, **fallas silenciosas** y **handoffs poco claros** **no aparecen en el IDE**; aparecen al modelar el **flujo de negocio**.
- Primero el flujo, después los marcos formales: el flujo mantiene el análisis aterrizado en lo que importa al negocio.

## 🪜 Los 4 pasos
1. **🗺️ Mapear el flujo**: un proceso con agentes, de inicio a fin; quién lo dispara, qué datos pasan y dónde entra el agente.
   *Ej.: Solicitud del cliente → Agente revisa datos → Agente responde → Aprobación humana → Actualización del sistema*
2. **📍 Marcar las interacciones** del agente con **personas**, **datos** y **sistemas** (apps, APIs, BD). Ahí es donde aparecen los riesgos.
3. **🔎 Aplicar el lente de amenazas** en cada punto: ¿qué puede salir mal?, ¿qué pasa si el agente decide mal o **actúa muy pronto o muy tarde**?, ¿**quién podría explotarlo**? → tabla Paso · Riesgo · Impacto.
4. **🛠️ Planear la respuesta** a cada riesgo:

| Respuesta | Qué es |
|---|---|
| 🔧 **Fix** | Ajustar permisos, añadir revisiones, limitar accesos |
| 👀 **Monitor** | Alertas, logs, revisiones periódicas |
| 📝 **Accept** | Documentar riesgos **de bajo impacto** para revisarlos luego |

Elegir los **3 riesgos principales** con una respuesta concreta cada uno.

| Paso | Riesgo | Respuesta | Impacto |
|---|---|---|---|
| Solicitud del cliente | Datos incompletos | **Fix**: campos obligatorios y validaciones | El agente recibe info completa |
| Agente revisa datos | **Acceso excesivo a API** | **Monitor**: alertas si accede fuera de los sistemas aprobados | Seguridad detecta accesos inusuales a tiempo |

Ejemplo práctico: [[📭 Escenario del reporte que desaparece]]. Riesgos a buscar: [[🕷️ Amenazas de seguridad para agentes]]. Parecido al [[🪜 Mapeo de procesos para agentes]] y al [[🧮 Marco PBTD para riesgos de agentes]].

> ⚠️ Ojo de examen: **STRIDE** no ve riesgos de **flujo** (aprobaciones faltantes, fallas silenciosas, handoffs). Los 4 pasos: **mapear → marcar interacciones (personas, datos, sistemas) → lente de amenazas → respuesta**. Respuestas: **Fix, Monitor, Accept**.

## 🔁 Repaso #flashcards
¿Qué significa STRIDE?::Spoofing, Tampering, Repudiation, Information disclosure, Denial of service, Elevation of privilege.
¿Qué riesgos no detecta STRIDE ni el IDE pero sí el threat modeling del flujo?::Aprobaciones faltantes, fallas silenciosas y handoffs poco claros.
¿Cuáles son los 4 pasos del threat modeling simplificado de un flujo con agentes?::Mapear el flujo, marcar las interacciones, aplicar el lente de amenazas y planear la respuesta.
¿Con qué tres cosas se marcan las interacciones de un agente en el flujo?::Personas, datos y sistemas.
¿Cuáles son las tres respuestas posibles a un riesgo identificado?::Fix (corregir), Monitor (vigilar) y Accept (aceptar y documentar si es de bajo impacto).
¿Qué tipo de riesgos se aceptan en el threat modeling?::Los de bajo impacto, documentándolos para revisarlos después.
