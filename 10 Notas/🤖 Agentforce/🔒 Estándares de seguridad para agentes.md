---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 🔒 Estándares de seguridad para agentes

## 📜 AI Acceptable Use Policy
Salesforce publicó su **AI AUP** para alinearse con la industria y sus socios y proteger a los clientes. Antes de publicarla consultó a un subcomité de su **Ethical Use Advisory Council**, socios, líderes de la industria y desarrolladores. Es **solo un punto de partida**: cada empresa debería crear **sus propias reglas o principios de IA**.

## 🧱 Estándares recomendados
| Categoría | Tipo | Recomendación |
|---|---|---|
| 🔑 **Access Control** | **Strict Access Controls** | Solo quien tenga **need to know** interactúa con los modelos. Identificar **todo el alcance y las acciones** del agente; para **acciones críticas**, ejecutar el agente con **usuarios de servicio individuales** para controles granulares (ver [[🔐 Permisos del usuario del agente]]) |
| | **Monitoring and Auditing** | **Alertas** y auditoría del acceso a modelos para detectar uso no autorizado |
| 💾 **Data Protection** | **Integrity Controls** | Controles de integridad para datos internos y de clientes: seguridad de apps, **backup y restore**, configuraciones base |
| 🙋 **Responsible Use** | **Customer Data Handling** | Datos personales solo con **fines legítimos**, **aviso y consentimiento** |
| | **Customer Transparency** | Los servicios **no hacen inferencias invisibles** para el cliente |
| | **Content Moderation** | **Filtro de moderación** sobre la IA generativa, **activo por defecto** |
| | **Ethical Use** | Guías de uso ético que respeten privacidad y seguridad |

Ver [[🏛️ Guardrails de plataforma y de Agentforce]], [[🎯 Red-teaming de IA]] y [[🔑 Mínimo privilegio en agentes]].

> ⚠️ Ojo de examen: para **acciones críticas** → el agente corre con **usuarios de servicio individuales** (control granular). **Content moderation activa por defecto**. **Customer transparency** = nada de inferencias invisibles al cliente.

## 🔁 Repaso #flashcards
¿En qué tres categorías se agrupan los estándares de seguridad para agentes?::Access control, data protection y responsible use.
¿Qué se recomienda para las acciones críticas de un agente?::Ejecutar el agente en contextos de usuario de servicio individuales para un control de acceso granular.
¿Qué exige el estándar de Customer Transparency?::Que los servicios no hagan inferencias invisibles para el cliente.
¿Cómo debe configurarse la moderación de contenido sobre IA generativa?::Con un filtro de moderación activo por defecto donde exista.
¿La AI AUP de Salesforce basta como política de IA de tu empresa?::No, es un punto de partida; cada empresa debería crear sus propias reglas o principios de IA.
