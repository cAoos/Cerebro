---
tipo: nota
tema: seguridad
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🎚️ Autoridad progresiva

Ajustar el **nivel de fricción** al **impacto potencial** de la acción. Leer es poco riesgoso; **escribir necesita más protección**. Es parte del [[🔑 Mínimo privilegio en agentes|mínimo privilegio]].

| Impacto | Gobierno | 🧪 Ejemplo (banco) |
|---------|----------|---------------------|
| 🟢 **Bajo** | Acción **limitada y reversible**, con entradas validadas | Consultar el **saldo**: solo lectura, sin permisos extra |
| 🟡 **Moderado** | **Mostrar el cambio propuesto** y pedir **confirmación** | **Disputa** de un cargo desconocido: el agente propone la solución y un humano la aprueba |
| 🔴 **Alto** | Pasar por **aprobación humana** o un proceso de negocio establecido | **Subir el cupo** de la tarjeta: flujo formal de aprobación con supervisor |

> 💡 Lo **irreversible o muy sensible** mejor **no dárselo al agente**, salvo con autorización fuerte, verificación independiente y forma de recuperar.

> [!note]- ✍️ Toda acción de escritura debe definir
> - Quién puede pedirla
> - Qué registros y campos cambia, y qué valores son válidos
> - Condiciones de negocio, y si pide confirmación o aprobación
> - Cómo evitar duplicados
> - Cómo se registra, monitorea y **revierte**

> ⚠️ Ojo de examen: "el agente propone y el usuario confirma" → **impacto moderado**. "Requiere aprobación del supervisor" → **impacto alto**.

Relacionado: [[🤝 Modelo de colaboración humano-IA]] · [[🚧 Guardrails para agentes autónomos]].

## 🔁 Repaso #flashcards
¿Qué es la autoridad progresiva?::Ajustar la fricción (confirmación, aprobación) al impacto potencial de la acción del agente.
¿Qué gobierno lleva una acción de impacto moderado?::Mostrar el cambio propuesto y pedir confirmación del usuario.
¿Qué gobierno lleva una acción de alto impacto?::Pasar por aprobación humana o un proceso de negocio establecido.
