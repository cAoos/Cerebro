---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-06
---
# 📦 Mover un agente a producción

Las conexiones se configuran y prueban **en sandbox**. Antes de salir hay que **probar de punta a punta en cada canal**, incluidos los **adaptive response formats**, y luego **mover el agente** a staging o producción.

## ✅ Prerrequisitos
- 🧪 **Un agente construido y probado**: el despliegue asume que ya funciona.
- 🧑‍💻 **Un usuario de agente**: el Service Agent corre como un **usuario de integración** dedicado; su **perfil y permisos** deciden a qué accede (ver [[🔐 Permisos del usuario del agente]]).
- 📺 **Canales listos**: cada uno tiene lo suyo (p. ej. un sitio donde embeber el chat).

## 🪜 Pasos para desplegar a la org destino
1. **Recuperar la metadata** del sandbox con **Salesforce CLI** y generar el **paquete** del agente. Incluir **Apex, flows y prompt templates** de las acciones, y los **permission sets** del usuario del agente.
2. Verificar que hay **licencias** en la org destino.
3. Verificar que **Einstein, Agentforce y Data 360** están **habilitados**.
4. **Crear el usuario del agente** en la org destino.
5. Si se usan **Enhanced Chat, Embedded Service Deployments u Omni-Channel Flows**, desplegarlos también.
6. **Desplegar la metadata de Agentforce** con Salesforce CLI.
7. Verificar que el agente está **activo**.
8. **Asignar los permission sets** desplegados al usuario del agente.
9. Revisar que cada flow tenga **activa la versión correcta**.
10. Si hay **Embedded Service Deployment**, **publicarlo** en la org destino.

Después: revisar **subagentes, instrucciones, variables y filtros**, los **permisos**, y que el agente **responda**. Lo que sigue es **Observe** (monitoreo, badge *Agent Analytics and Monitoring*).

Ver [[🚀 Estrategia de despliegue de un agente]] y [[🧾 Estructura de un Agent Script]] (otra forma de portar agentes).

> ⚠️ Ojo de examen:
> - Se mueve con **metadata + Salesforce CLI**.
> - El paquete lleva **Apex, flows, prompt templates y permission sets**.
> - El **usuario del agente se crea** en la org destino; **no viaja** en el paquete.
> - Hay que confirmar **licencias** y que **Einstein, Agentforce y Data 360** estén encendidos.
> - Después: **activar** el agente, **asignar los permission sets**, revisar la **versión activa de los flows** y **publicar** el Embedded Service Deployment.

> 🚚 Para una plantilla de prompt sola: [[🚚 Desplegar una plantilla de prompt a producción]].

## 🔁 Repaso #flashcards
¿Con qué herramienta se mueve un agente de sandbox a producción?::Con Salesforce CLI, recuperando y desplegando la metadata.
¿Qué debe incluir el paquete de un agente?::Apex, flows y prompt templates de sus acciones, y los permission sets del usuario del agente.
¿Qué hay que verificar que esté habilitado en la org destino antes de desplegar un agente?::Einstein, Agentforce y Data 360 (además de las licencias).
¿El usuario del agente viaja en el paquete?::No, hay que crearlo en la org destino y asignarle los permission sets desplegados.
¿Cuáles son los 3 prerrequisitos para desplegar un agente?::Un agente construido y probado, un usuario de agente con los permisos correctos y los canales listos.
¿Qué hay que publicar en la org destino si el agente usa chat web?::El Embedded Service Deployment.
