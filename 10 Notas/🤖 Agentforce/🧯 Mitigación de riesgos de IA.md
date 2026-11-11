---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-10-30
---
# 🧯 Mitigación de riesgos de IA

Después de evaluar riesgos en la [[⚖️ Gobernanza de IA]], se aplican salvaguardas por tipo de riesgo. Es **imposible evitarlos todos**: la meta es **identificarlos y gestionarlos con confianza**.

| Tipo de riesgo | Estrategias de mitigación |
|---|---|
| 🔐 **Técnico y seguridad** | Políticas y protocolos de seguridad · **detección de anomalías** y planes de respaldo · infraestructura, tenancy y hosting seguros · **red-teaming** de ciberseguridad |
| 🗄️ **Datos y privacidad** | **Controles de acceso** · **anonimización y cifrado** · auditorías de datos · políticas contra mal uso · estándares de calidad · limpieza y validación |
| 🤝 **Ético y seguridad** | Principios de IA responsable · políticas de uso aceptable · **red-teaming ético** · herramientas de **sesgo** · benchmarking de modelos · **transparencia** (explicabilidad, **citas**) · **marcas de agua** en contenido generado · **feedback** · **audit logs** |
| ⚙️ **Operativo** | Evaluaciones de riesgo · **planes de respuesta a incidentes** · gestión del cambio · documentación y educación · métricas y monitoreo · revisiones éticas internas |
| 📜 **Cumplimiento y legal** | Protocolos y capacitación de cumplimiento · consultas legales y contratos |

En Salesforce muchas de estas ya vienen en el [[🛡️ Einstein Trust Layer]] (enmascaramiento, toxicidad, audit trail, zero data retention).

> ⚠️ Ojo de examen: asocia cada salvaguarda con su tipo. **Marcas de agua, citas, sesgo, red-teaming ético** → ético. **Anonimización, cifrado, controles de acceso** → datos y privacidad. **Respuesta a incidentes, gestión del cambio** → operativo.

## 🔁 Repaso #flashcards
¿A qué tipo de riesgo corresponden las marcas de agua en contenido generado por IA?::Ético y de seguridad.
¿Qué estrategias mitigan riesgos de datos y privacidad?::Controles de acceso, anonimización y cifrado, auditorías, políticas contra mal uso, estándares de calidad, limpieza y validación.
¿Qué es red-teaming y en qué dos tipos aparece?::Atacar el sistema a propósito para encontrar fallas; aparece como red-teaming de ciberseguridad (técnico) y ético.
¿A qué tipo de riesgo pertenecen los planes de respuesta a incidentes?::Operativo.
