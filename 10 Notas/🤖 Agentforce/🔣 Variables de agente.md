---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-30
---
# 🔣 Variables de agente

Guardan y reutilizan valores en la lógica del agente y **controlan cómo decide**. Base del [[🎯 Determinismo en Agentforce|determinismo]].

- 🌍 **Son globales**: **cualquier [[🗂️ Subagentes|subagente]]** puede leerlas y escribirlas. No pertenecen a un subagente.
- ➕ Se crean en el Explorer → **Variables** → **New** → **Create Custom Variable**: nombre/API name, **tipo de dato** (Number, Boolean…), descripción y **valor por defecto**.
- 🔄 **Se reinician en cada sesión** al valor por defecto.

![[determinismo-variable-creada.jpg]]

## ✍️ Llenarlas desde una acción
En **Script**, debajo de la acción:
```
Get_Customer_Details: @actions.Get_Customer_Details
    with email = ...
    with memberNumber = ...
    set @variables.LifetimeValue = @outputs.contact.data.Lifetime_Value__c
```
`with` = inputs de la acción · `set @variables.X = @outputs...` = guardar un output en la variable.

En Canvas también existe el **follow-up action → Set a variable** (ej: `isCreditIssued = True` después de dar el crédito). Ver [[🚫 Filtros de acciones]].

## 🔘 Valor por defecto
Los **Boolean sin default quedan en False** automáticamente, pero conviene **declararlo explícito** para que otros entiendan la lógica condicional.

![[determinismo-variable-boolean.png]]

## 👁️ Verlas en Preview
En **Preview** → pestaña **Variables**: el valor de cada variable **antes y después** de cada paso. Ver [[🧪 Probar un agente en el Builder]].

![[determinismo-variables-preview.jpg]]

> ⚠️ Ojo de examen: variables **globales** (todos los subagentes) y **por sesión** (se reinician). Para guardar el output de una acción: `set @variables.X = @outputs.Y`. Para ver sus valores al probar: pestaña **Variables** del Preview.

## 🔁 Repaso #flashcards
¿Las variables de agente pertenecen a un subagente?::No, son globales: cualquier subagente puede leerlas y escribirlas.
¿Cómo se guarda el output de una acción en una variable en Agent Script?::set @variables.Nombre = @outputs.ruta.del.valor
¿Qué valor toma un Boolean sin default?::False, pero conviene declararlo explícito para claridad.
¿Qué pasa con las variables al empezar una nueva sesión?::Se reinician a su valor por defecto.
¿Dónde ves el valor de las variables mientras pruebas?::En Preview, pestaña Variables: muestra el valor antes y después de cada paso.
