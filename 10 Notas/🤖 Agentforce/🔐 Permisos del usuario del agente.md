---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-30
---
# 🔐 Permisos del usuario del agente

El agente actúa como un **usuario de agente** (ej: **EinsteinServiceAgent User**) y **solo ve lo que ese usuario puede ver**. Los usuarios **no tienen acceso automático a campos custom**.

## 🛠️ Darle acceso
Setup → **Users** → usuario del agente → **Permission Set Assignments** → su permission set (ej: Service Agent Permissions) → **Object Settings** → objeto → **Edit**:
- 👁️ **Campo custom** que el agente debe leer → acceso de **lectura** (FLS).
- ✍️ **Objeto** donde el agente crea registros → permisos de objeto **Read + Create** y **Edit** en los campos que llena.

![[determinismo-permiso-campo.jpg]]
![[determinismo-permiso-objeto.jpg]]

## 🌊 Ojo con los flows compartidos
Si cambias un flow que usan las acciones (ej: agregar `Lifetime_Value__c` a Get Customer Details) y activas la nueva versión, **todos los agentes que usan ese flow** toman la nueva versión. Para no afectarlos, guarda el flow modificado como **un flow nuevo**.

Ver [[🔑 Mínimo privilegio en agentes]].

> ⚠️ Ojo de examen: si el agente **no ve un campo o no puede crear un registro**, revisa los **permisos del usuario del agente** (permission set: objeto + FLS). Los campos custom **no son visibles por defecto**.

> 📮 En el SDR, el agent user se crea desde Salesforce Go (**+ New User**) y la configuración se aplica sola; si eliges uno existente, el setup verifica sus permisos: [[🛠️ Configurar Agentforce SDR paso a paso]].

## 🔁 Repaso #flashcards
¿Con qué permisos actúa un agente de servicio?::Con los del usuario de agente asignado (ej: EinsteinServiceAgent User) y su permission set.
¿Por qué un agente podría no ver un campo custom?::Porque los usuarios no tienen acceso automático a campos custom; hay que dar FLS de lectura al usuario del agente.
¿Qué permisos necesita el agente para crear registros de un objeto?::Read y Create en el objeto, y Edit en los campos que llena.
¿Qué pasa si activas una nueva versión de un flow usado por acciones de agente?::Todos los agentes que usan ese flow pasan a la nueva versión; para no afectarlos, guárdalo como flow nuevo.
