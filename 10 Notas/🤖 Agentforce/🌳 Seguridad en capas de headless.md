---
tipo: nota
tema: seguridad
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🌳 Seguridad en capas de headless

[[🔓 Headless en Salesforce (AIforce)|Headless]] abre nuevos lugares desde donde usuarios, apps y agentes piden acceso. El admin **no necesita volverse ingeniero de seguridad**: las preguntas son las mismas de siempre. *¿Quién necesita acceso, a qué nivel y qué puede hacer?*

## 🌳 La metáfora del árbol
![[headless-arbol-seguridad.png|500]]

Un árbol puede verse sano, pero si las raíces son débiles se cae con el primer viento.

| | Parte | Capa | Qué incluye |
|---|-------|------|-------------|
| 🍃 | **Ramas y hojas** | Superficie visible | Slack, chats, acciones visibles del usuario |
| 🪵 | **Tronco** | [[🛡️ Einstein Trust Layer]] | Media **todo el tráfico**, enmascara datos y asegura la ejecución |
| 🌱 | **Raíces** | Base invisible | Políticas por rol, reglas de acceso y permisos |

> [!note]- 🌱 Lo que hay en las raíces (lo que no se ve)
> - 🪪 **Identidad y autenticación**: quién llama y cómo lo probó
> - 🔐 **Controles de acceso y permisos**: qué datos puede leer o escribir
> - 🧾 **FLS**: qué campos del registro ve
> - 👔 **RBAC**: qué acciones puede hacer un rol
> - 📜 **Compliance y audit trails**: registro de cada acceso
> - 🧬 **Data lineage**: de dónde vienen los datos
> - 📡 **Monitoreo en tiempo real**: detecta accesos anómalos
> - 🌐 **Seguridad de red**: cifrado en tránsito, aislamiento
> - 🚫 **Data loss prevention**: evita que datos sensibles salgan de los límites aprobados

Con una integración **DIY** puedes hacer árboles bonitos, pero **tú construyes todas las raíces**: si falta una, el agente puede compartir o borrar lo que no debía. Salesforce ya las trae, basado en dos principios:
1. 🚪 [[🚪 Open access, not open bypass]]
2. 🔑 [[🔑 Mínimo privilegio en agentes]]

## 🧭 Gobierno y monitoreo en 4 pasos
**Gobierno** = políticas de quién (humano o agente) accede a qué. **Monitoreo** = observar para detectar y corregir rápido.

1. 🎯 **Know the task**: caso de uso, dueño, usuarios, datos y acciones.
2. 🔒 **Limit access**: solo el acceso que la tarea necesita.
3. 👀 **Monitor**: saber qué es normal y qué pasos críticos revisar ([[📡 Monitoreo de headless]]).
4. 🛑 **Stop issues**: cómo detener la tarea, a quién llamar y cómo cortar el acceso ([[🚨 Respuesta a incidentes headless]]).

> ⚠️ Ojo de examen: en el árbol, la **Trust Layer es el tronco** (media todo el tráfico). Las **raíces** son identidad, permisos, FLS y RBAC.

## 🔁 Repaso #flashcards
¿Qué representa cada parte del árbol en seguridad headless?::Hojas: superficie visible (Slack, chat) · Tronco: Einstein Trust Layer · Raíces: permisos, identidad, FLS, RBAC.
¿Cuáles son los 4 pasos de gobierno y monitoreo headless?::Know the task, Limit access, Monitor, Stop issues.
¿Por qué es riesgosa una integración DIY con IA?::Porque hay que construir todas las raíces de seguridad (identidad, permisos, auditoría…); si falta una, el agente puede filtrar o borrar datos.
