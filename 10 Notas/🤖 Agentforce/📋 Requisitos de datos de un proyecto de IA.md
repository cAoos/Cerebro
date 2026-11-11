---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-10-31
---
# 📋 Requisitos de datos de un proyecto de IA

**Data-ready** = los datos del proyecto son **precisos, disponibles, accesibles y gobernados de forma segura**. La calidad de datos es una de las **mayores barreras** para la IA.

💡 **No persigas datos perfectos**: muchos proyectos se atascan ahí. Fija metas **razonables** y usa la etapa **Build** para cerrar brechas. Base general en [[🧹 Preparación de datos para IA]].

## 1️⃣ Inventario de datos
Qué datos necesitas · dónde están · y para cada uno: **tipo** ([[🗂️ Datos estructurados, semiestructurados y no estructurados|estructurado o no]]), **frecuencia de actualización** (tiempo real, diaria, estática), **acceso**, **gobierno** y **consideraciones**.

| Dato | Fuente | Tipo | Actualización | Ojo |
|---|---|---|---|---|
| Contactos | CRM | Estructurado | Diaria | Fechas MM/DD/YY |
| Reservas | Reserv-o-matic (externo) | Estructurado | **Tiempo real** | Fechas **DD/MM/YY** ⚠️ |
| Excursiones | CRM | Estructurado | Diaria | Fechas MM/DD/YY |

## 2️⃣ Calidad y limpieza
**Limpiar** = corregir o quitar datos incorrectos, corruptos, mal formateados, **duplicados** o **incompletos**, y cerrar brechas.

Orden de limpieza: 🥇 **alta prioridad + bajo esfuerzo** → 🥈 alta prioridad + alto esfuerzo → 🥉 baja prioridad si sobra tiempo.

🏝️ Becca unificó el formato de fechas y se dio cuenta de que **solo necesitaba las reservas futuras**: entender los requisitos **reduce el trabajo**.

## 3️⃣ Migrar e integrar
- **Migrar** = traer datos de varias fuentes a una central (en Salesforce, traer lo externo a Salesforce).
- **Integrar** = combinarlos en una **vista unificada**.
- **Solo lo que el proyecto necesita** (Becca quitó el campo Notes).

En Data 360: **Data Stream** para traer los datos externos + **Identity Resolution** para unir la Sofia de Salesforce con la de Reserv-o-matic. Ver [[☁️ Data 360 para agentes]].

## 4️⃣ Gobierno de datos
**Data 360 Governance**: políticas de acceso, **enmascaramiento dinámico** de datos y más.

## 5️⃣ Plan de analítica
Cómo medir las metas del proyecto para **demostrar ROI**. Ej: tiempo en pantalla del front desk antes/después, y encuesta opcional de satisfacción.

> ⚠️ Ojo de examen: **data-ready** = preciso, disponible, accesible y gobernado. No buscar perfección. Limpiar primero **alta prioridad / bajo esfuerzo**. Unir el mismo cliente de dos fuentes = **Identity Resolution**; traer datos externos = **Data Stream**.

## 🔁 Repaso #flashcards
¿Qué significa que una organización esté data-ready?::Que los datos del proyecto son precisos, disponibles, accesibles y gobernados de forma segura.
¿Qué preguntas responde un inventario de datos?::Qué datos, dónde están, tipo, frecuencia de actualización, cómo se accede, si tienen gobierno y qué consideraciones hay.
¿En qué orden se limpian los datos?::Alta prioridad y bajo esfuerzo, luego alta prioridad y alto esfuerzo, luego baja prioridad si hay tiempo.
¿Qué diferencia hay entre migrar e integrar datos?::Migrar es traerlos a una fuente central; integrar es combinarlos en una vista unificada.
¿Qué herramienta de Data 360 une al mismo cliente que viene de dos fuentes?::Identity Resolution.
¿Para qué sirve el plan de analítica?::Para medir si se cumplen las metas y demostrar el ROI del proyecto.
