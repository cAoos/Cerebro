---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# 🎒 Anatomía de una skill

Una **skill** es una capacidad especializada que se invoca desde un asistente de IA como Claude o Cursor: un **flujo prearmado con expertise de dominio**. Parte del [[🧳 Headless Toolkit]].

- ⌨️ Se invoca de forma estándar: **`/skill-name`**.
- 🧠 Es **context aware**, usa **conocimiento especializado** y es **componible**.
- 🔁 Convierte un flujo de **varios pasos en un solo comando**. Ejemplo: en vez de "lee los archivos, analízalos y escribe un reporte", **`/code-review`** detecta los archivos cambiados, los analiza con criterios de seguridad y calidad, revisa la cobertura de pruebas y entrega el reporte.

## 📁 Qué hay dentro
| Archivo | Para qué | ¿Obligatorio? |
|---|---|---|
| 📄 **SKILL.md** | Nombre, **descripción** e **instrucciones** para que el agente complete la tarea | ✅ **Sí** |
| 📚 **Reference files** | Documentos de apoyo que extienden la skill | Opcional |
| 🧪 **Scripts** | Código ejecutable para automatizar tareas repetitivas, validar salidas o procesar datos | Opcional |
| 📏 **Evals** | **Pruebas sistemáticas** que miden si el agente **dispara, sigue y ejecuta** las instrucciones | Opcional |

**Distribución:** archivos sueltos en un repositorio con acceso autenticado, o **agrupadas como plugins**.

## ☁️ Skills de Salesforce
- Colección curada en el repo de GitHub **sf-skills**: Lightning apps, Apex, Flow, Data 360…
- Vienen **auto-instaladas y auto-activadas en Agentforce Vibes**. En Claude o Cursor: **`npx skills add forcedotcom/sf-skills`**.
- Ejemplo: **platform-sandbox-configure** lista el inventario de sandboxes, informa el estado de uno, crea uno nuevo y lo **refresca** con datos de producción.
- También existe el **Salesforce Development Plugin for Claude Code**.

Las skills para construir agentes de Agentforce son las [[🛠️ ADLC Skills]].

> ⚠️ Ojo de examen: el único archivo **obligatorio** es **SKILL.md**. Las **evals** prueban si el agente dispara y sigue la skill. Las sf-skills vienen **auto-activadas en Agentforce Vibes**.

> ⚡ Vista de usuario de negocio: una skill es un **prompt template prearmado que se ejecuta con un clic** (p. ej. *View Top Opportunities*). Ver [[🪟 Cuatro pilares técnicos de headless]].

## 🔁 Repaso #flashcards
¿Qué es una skill en un asistente de IA?::Un flujo prearmado con expertise de dominio que se invoca con /skill-name; es context aware y componible.
¿Qué archivo es obligatorio en el directorio de una skill?::SKILL.md, con nombre, descripción e instrucciones.
¿Qué archivos opcionales puede tener una skill?::Reference files, scripts y evals.
¿Qué son las evals de una skill?::Pruebas sistemáticas que miden si el agente dispara, sigue y ejecuta las instrucciones de la skill.
¿Cómo se distribuyen las skills?::Como archivos en un repositorio con acceso autenticado o agrupadas en plugins.
¿Dónde vienen auto-instaladas las sf-skills y cómo se instalan en otro asistente?::En Agentforce Vibes; en Claude o Cursor con npx skills add forcedotcom/sf-skills.
¿Qué hace la skill platform-sandbox-configure?::Lista sandboxes, informa su estado, crea uno nuevo y lo refresca con datos de producción.
