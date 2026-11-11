# Convenciones del vault

## Carpetas
| Carpeta | Qué va |
|---------|--------|
| `00 Inbox` | Captura rápida. Se procesa cada semana |
| `10 Notas` | Notas atómicas. Una subcarpeta por área grande (`🤖 Agentforce`); dentro, todas planas |
| `20 Mapas` | MOCs |
| `30 Fuentes` | Una nota por módulo, curso, libro o video |
| `40 Proyectos` | Un proyecto por bloque mensual |
| `90 Plantillas` | Plantillas |
| `99 Adjuntos` | Imágenes y archivos |

## Nombres
| Tipo | Formato | Ejemplo |
|------|---------|---------|
| Nota atómica | Emoji + concepto corto, solo la primera letra en mayúscula | `💬 Comentarios en Apex` |
| Fuente | `Origen - Nombre oficial` (Trailhead, Doc, Curso, Libro, Video, Artículo) | `Trailhead - Apex Basics for Admins` |
| Mapa | `MOC Tema` | `MOC Platform Developer` |
| Proyecto | `AAAA-MM Nombre` | `2026-10 Platform Developer` |
| Inbox | `AAAA-MM-DD tema breve` | `2026-10-12 dudas triggers` |
| Adjunto | `tema-descripcion.ext` en minúsculas | `apex-orden-de-ejecucion.png` |
| Plantilla | `Plantilla - Tipo` | `Plantilla - Nota atómica` |

Reglas de los títulos:
- Las notas atómicas empiezan con **un emoji que represente la idea**. Al enlazar, basta con escribir la palabra y el autocompletado encuentra la nota.
- Secciones fijas de la nota: `## 🧪 Ejemplo` y `## 🔁 Repaso`. Dentro del texto, emojis solo donde ayuden a escanear (⚠️ ojo de examen, 💡 tip, ✅/❌ correcto/incorrecto).
- En español, con los términos técnicos como aparecen en Salesforce (Queueable, trigger, Developer Console).
- Sin `: / \ # | ^ [ ]`.
- Si el título necesita un "y", probablemente son dos notas.

## Propiedades
| Propiedad | Valores |
|-----------|---------|
| `tipo` | `nota` · `fuente` · `mapa` · `proyecto` · `inbox` |
| `estado` | `nueva` → `repasada` → `dominada` |
| `debil` | `true` si salió flojo en un examen de práctica |
| `tema` | lista cerrada, abajo |

**Temas permitidos** (agregar aquí antes de usar uno nuevo):
`apex-fundamentos` · `apex-asincrono` · `triggers` · `soql` · `dml` · `testing` · `lwc` · `flow` · `seguridad` · `modelo-datos` · `despliegue` · `debug` · `agentforce` · `prompts` · `data-360` · `trust-layer`

## Etiquetas
Solo `#flashcards`. Todo lo demás va en propiedades.
