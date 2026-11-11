---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-09
---
# 🏧 Agentes financieros en acción

Dos escenas de **Cumulus Cloud Bank**, que arrancó con las plantillas de [[🧩 Skills de Agentforce for Financial Services]].

## 🧑‍💼 Service rep: reversar un cargo por sobregiro
**Antes:** el cliente llama por un cargo de sobregiro inesperado. El rep salta entre páginas, historial de casos, transacciones y políticas del banco, y el cliente espera con música de fondo.

**Con Banking Employee Service Assistance:** el rep solo pide *"reversa el cargo por sobregiro de este cliente"*.
1. 🧠 El agente entiende el contexto y **planea dinámicamente** la resolución, siguiendo las instrucciones.
2. 📂 **Get financial accounts** del cliente.
3. 💸 **Get transactions**: trae los cargos desde el **core bancario**.
4. ✅ **Con el consentimiento del rep**, crea el **fee reversal case** con todos los detalles.

Todas las acciones vienen de la plantilla y están integradas con el modelo de datos de Agentforce Financial Services.

## 🙋 Cliente: elegir un préstamo
Con **Loan Product Assistance** en la web del banco:
1. *"¿Qué tipos de préstamo ofrecen?"* → lista de tipos.
2. Explora un producto y pregunta el **monto máximo** → el agente le pide la **cuota mensual deseada y el plazo**, y le da un **estimado**.
3. Pide **comparar** tipos de préstamo por un atributo, como la **tasa de interés más baja**.
4. Termina sabiendo qué producto pedir, el monto estimado y la cuota.

Resultado: el loan officer se dedica a la etapa *high-touch*, y suben la conversión y la satisfacción.

> ⚠️ Ojo de examen: el agente **planea** la secuencia de acciones a partir de una petición en lenguaje natural. Cuando la acción cambia algo, como crear el caso de reversa, la pide **con consentimiento del humano**. El agente de cliente **desvía casos**; el de empleado **acelera** los que llegan.

Parte de [[💳 Agentforce for Financial Services]]

## 🔁 Repaso #flashcards
¿Qué acciones encadena el agente para reversar un cargo por sobregiro?::Get financial accounts → get transactions (core bancario) → crear fee reversal case con consentimiento del rep.
¿Qué datos pide Loan Product Assistance para estimar el monto máximo?::La cuota mensual deseada y el plazo de pago.
¿Qué beneficio trae Loan Product Assistance al banco?::Los loan officers se enfocan en interacciones high-touch y suben conversión y satisfacción.
