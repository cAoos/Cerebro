---
tipo: nota
tema: seguridad
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🚨 Respuesta a incidentes headless

Cada capacidad headless en producción necesita un **plan de respuesta**, integrado al proceso de incidentes de la organización. Tiene **5 fases**:

```text
🔍 Triage ─► 🧯 Contain ─► 🕵️ Investigate ─► 🔧 Fix & Recover ─► 📚 Learn
```

| | Fase | Qué se hace |
|---|------|-------------|
| 🔍 | **Triage** | ¿Es normal, un error de configuración o un problema de seguridad? Reunir datos clave (cuándo, qué app, qué datos). **No esperar información perfecta** si hay datos sensibles en riesgo |
| 🧯 | **Contain** | La acción **más directa** para cortar el riesgo: deshabilitar una tool, quitar acceso, desactivar un usuario. **Registrar quién aprobó** y qué se apagó |
| 🕵️ | **Investigate** | Guardar evidencia **antes de que se borren los logs**, armar una línea de tiempo y compartir solo con quien corresponde |
| 🔧 | **Fix & Recover** | Arreglar **antes** de restaurar: corregir permisos amplios, registros afectados, volver a probar. Restaurar **de a poco**, empezando por la capacidad más pequeña validada |
| 📚 | **Learn** | Documentar **sin culpables**, identificar el control que faltó, asignar cada mejora a un dueño con fecha |

> 💡 Un incidente **no se cierra cuando vuelve el servicio**, sino cuando se **verifican las mejoras** acordadas.

## 🧪 Ejemplo
Un agente por MCP empieza a actualizar casos que no debía. **Triage**: no es normal. **Contain**: el admin deshabilita ese MCP server (o revoca los tokens OAuth). **Investigate**: guarda los Event Log Files. **Fix**: cambia a un servidor read-only y vuelve a probar. **Learn**: faltaba una named query más restrictiva.

> ⚠️ Ojo de examen: el **orden** de las fases, y que **contener va antes que investigar**.

Va con [[📡 Monitoreo de headless]].

## 🔁 Repaso #flashcards
¿Cuáles son las 5 fases de respuesta a incidentes headless?::Triage, Contain, Investigate, Fix & Recover, Learn.
¿Qué se hace en la fase Contain?::La acción más directa para cortar el riesgo (deshabilitar tool, quitar acceso, desactivar usuario) y registrar quién la aprobó.
¿Cuándo se cierra un incidente?::Cuando se verifican las mejoras acordadas, no cuando vuelve el servicio.
¿Cómo se restaura el servicio tras un incidente?::Gradualmente, empezando por la capacidad más pequeña validada y monitoreando antes de ampliar.
