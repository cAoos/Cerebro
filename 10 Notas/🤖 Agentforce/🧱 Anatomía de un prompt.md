---
tipo: nota
tema: prompts
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-26
---
# 🧱 Anatomía de un prompt

Un **prompt** es la instrucción que se le da a la IA o a un agente. **Cuanto más específico, mejor el resultado.**

## 🧩 Los seis componentes
| # | Componente | Qué responde |
|---|-----------|--------------|
| 1 | 🎭 **Role** | ¿Como quién debe actuar la IA? |
| 2 | 🧭 **Context** | ¿Qué información de fondo necesita para entender? |
| 3 | 🎯 **Task / Goal** | ¿Qué quiero que haga? |
| 4 | 📋 **Instructions** | ¿Cómo quiero que lo haga? |
| 5 | 📄 **Format** | ¿En qué formato debe responder? |
| 6 | 🚧 **Constraints** | ¿Qué límites o reglas debe respetar? |

## 🧪 Ejemplo
```md
Role: You are a customer service manager
Context: This is a support ticket from a frustrated customer who has been waiting 5 days for a response
Task: Write a follow-up email that addresses their concern and offers a solution
Instructions: Use a professional but empathetic tone. Reference the customer's previous message.
Format: Return as plain text
Constraints: Keep the email under 200 words
```

## ✂️ Triple comillas: separar datos de instrucciones
Las `"""` encierran los **datos** para que la IA no los confunda con las **instrucciones**.

> [!example]- 🏨 Ejemplo completo: Tranquil Trails Resort
> ```
> Role: You are a guest services manager for Tranquil Trails Resort
> Context: Luxury mountain resort known for hiking, spa services, and farm-to-table dining. This guest has just completed their stay.
> Task: Write a thank-you email to send after a guest checks out
> Instructions:
> - Thank them, mention specific activities, reference their comment
> - Include a special offer for their next visit; warm, personal tone
> Format: Professional email, subject line included, body text only (no HTML)
> Constraints: Under 200 words; personal, not generic
> """
> Guest Details:
> - Name: Sarah Martinez · Stayed: 3 nights (March 10-13) · Room: Mountain View Suite
> - Activities: Spa treatments, guided hiking tour, farm-to-table dinner
> - Comment: "Best vacation ever. Can't wait to come back!"
> """
> ```

Versión corta de esta idea en [[🤝 Modelo de colaboración humano-IA]]. Cómo escribirlos bien: [[✨ Buenas prácticas de prompts]].

## 🔁 Repaso #flashcards
¿Cuáles son los seis componentes de un buen prompt?::Role, Context, Task/Goal, Instructions, Format y Constraints.
¿Para qué sirven las triple comillas en un prompt?::Para separar los datos de las instrucciones y que la IA no los confunda.
