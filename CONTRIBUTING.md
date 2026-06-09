# Guía de Contribución

¡Gracias por querer compartir tu experiencia! Este documento explica cómo contribuir una experiencia docente, qué convenciones seguir y cómo funciona el proceso de revisión.

---

## Índice

- [Guía de Contribución](#guía-de-contribución)
  - [Índice](#índice)
  - [Antes de empezar](#antes-de-empezar)
  - [Cómo aportar una experiencia](#cómo-aportar-una-experiencia)
    - [Opción A: Pull Request (recomendada)](#opción-a-pull-request-recomendada)
    - [Opción B: Issue](#opción-b-issue)
  - [Estructura de una experiencia](#estructura-de-una-experiencia)
    - [Frontmatter YAML](#frontmatter-yaml)
    - [Secciones](#secciones)
  - [Convenciones](#convenciones)
    - [Nombres de fichero](#nombres-de-fichero)
    - [Disciplinas SWEBOK](#disciplinas-swebok)
    - [Estado del documento](#estado-del-documento)
    - [Idioma](#idioma)
    - [Imágenes](#imágenes)
  - [Proceso de revisión](#proceso-de-revisión)
  - [Preguntas frecuentes](#preguntas-frecuentes)

---

## Antes de empezar

- Lee el [README](README.md) para entender el propósito y la estructura del repositorio.
- Consulta las [experiencias existentes](experiencias/) para hacerte una idea del nivel
  de detalle esperado.
- Comprueba que tu experiencia no está ya documentada (búsqueda por universidad,
  herramienta o asignatura).

---

## Cómo aportar una experiencia

### Opción A: Pull Request (recomendada)

Es la vía preferida si tienes experiencia con Git. Permite revisión directa sobre
el contenido y trazabilidad de los cambios.

**Pasos:**

1. Haz **fork** del repositorio y clónalo localmente:
```bash
   git clone https://github.com/sistedes-ia4sw/ai-se-learn.git
   cd ai-se-learn
```

2. Crea una rama descriptiva:
```bash
   git checkout -b experiencia/tu-universidad-tema-breve
```
   Ejemplo: `experiencia/unizar-copilot-code-review`

3. Copia la plantilla y renómbrala siguiendo las [convenciones de nombre](#nombres-de-fichero):
```bash
   cp plantillas/experiencia.md experiencias/titulo-de-tu-experiencia.md
```

4. Rellena el fichero: primero el frontmatter YAML y luego cada sección.
   Los campos marcados con `*` son **obligatorios**.

5. Si incluyes imágenes, colócalas en `assets/img/` con un prefijo identificativo:
```bash
   assets/img/copilot-code-review-flujo.png
```

6. Haz commit y push:
```bash
   git add experiencias/titulo-de-tu-experiencia.md
   git add assets/img/   # si hay imágenes
   git commit -m "Nueva experiencia: Título descriptivo de tu experiencia"
   git push origin experiencia/tu-universidad-tema-breve
```

7. Abre un **Pull Request** contra `main` desde GitHub. Completa el checklist
   de la plantilla de PR antes de solicitar revisión.

---

### Opción B: Issue

Si no estás familiarizado con Git, puedes contribuir abriendo un Issue con la
etiqueta `nueva-experiencia`. Usa la plantilla de Issue proporcionada, que recoge
los mismos campos que la plantilla Markdown. Un mantenedor se encargará de crear
el fichero `.md` correspondiente y te acreditará como autor/a.

> [Abrir un Issue de nueva experiencia](../../issues/new?template=nueva-experiencia.yml&labels=nueva-experiencia)

---

## Estructura de una experiencia

Cada fichero sigue esta estructura:

### Frontmatter YAML

```yaml
---
titulo: "Título descriptivo de la experiencia"          # * obligatorio
universidad: "Nombre de la universidad"                  # * obligatorio
autores:                                                  # * obligatorio
  - nombre: "Nombre Apellidos"
    orcid: "0000-0000-0000-0000"                         # opcional pero recomendado
    email: "correo@universidad.es"                       # opcional
asignatura: "Nombre de la asignatura"                    # * obligatorio
curso: "2024-25"                                         # * obligatorio
estado: "publicada"                                      # * obligatorio: borrador | revisión | publicada
disciplinas_swebok:                                      # al menos una
  - Testing
  - Construction
herramientas_ia:                                         # al menos una
  - GitHub Copilot
nivel_educativo: "Grado"                                 # Grado | Máster | Posgrado
palabras_clave:
  - pair programming
  - revisión de código
---
```

### Secciones

| Sección | Contenido esperado |
|---|---|
| **1. Información General** | Contexto académico, número de estudiantes, modalidad |
| **2. Objetivos de la Innovación** | Conocimientos, habilidades y competencias perseguidas |
| **3. Metodología y Diseño** | Estrategia didáctica, herramientas, secuencia de actividades |
| **4. Implementación y Resultados** | Ejecución, participación, evidencias y datos |
| **5. Análisis Crítico y Reflexión** | Evaluación, desafíos, ética, lecciones aprendidas |
| **6. Guía de Replicabilidad** | Orientaciones para reproducir la experiencia |
| **7. Futuras Mejoras** | Propuestas de evolución y transferencia a otros contextos |

Las secciones 1–4 son **obligatorias** para que una experiencia sea aceptada.
Las secciones 5–7 son muy recomendables y aumentan significativamente el valor
de la contribución.

---

## Convenciones

### Nombres de fichero

Usa **kebab-case** basado en la herramienta principal y el contexto de uso:

```bash
chatgpt-generacion-casos-prueba.md
copilot-pair-programming-construccion.md
claude-revision-codigo-arquitectura.md
```

Evita incluir el nombre de la universidad en el fichero: esa información ya
está en el frontmatter y los nombres de fichero deben ser descriptivos del
contenido, no del origen.

### Disciplinas SWEBOK

Usa **exactamente** estos valores en el campo `disciplinas_swebok`:

`Requirements` · `Architecture` · `Design` · `Construction` · `Testing` ·
`Operations` · `Maintenance` · `Configuration Management` · `Management` ·
`Process` · `Models and Methods` · `Quality` · `Security`

Cualquier valor fuera de esta lista será solicitado como corrección durante
la revisión.

### Estado del documento

| Valor | Significado |
|---|---|
| `borrador` | En elaboración, no listo para revisión |
| `revisión` | Listo para ser revisado por los mantenedores |
| `publicada` | Revisado y aceptado |

Cuando abras un PR, el estado debe ser `revisión`.

### Idioma

Las experiencias pueden redactarse en **español** o en **inglés**. Los nombres
de los campos del frontmatter deben mantenerse en español tal como están
definidos en la plantilla, para garantizar la compatibilidad con las consultas
Dataview.

### Imágenes

- Formato preferido: PNG o SVG. Evita JPEGs para capturas de pantalla.
- Resolución mínima recomendada: 1200px de ancho.
- Prefijo obligatorio en el nombre: identifica tu experiencia.

```bash
assets/img/copilot-pair-programming-flujo.png
assets/img/copilot-pair-programming-resultados.png
```

- Referencia con ruta relativa desde el fichero de experiencia:
```markdown
  ![Flujo de trabajo](../assets/img/copilot-pair-programming-flujo.png)
```

---

## Proceso de revisión

1. Al abrir un PR, GitHub asigna automáticamente revisores del equipo
   `@sistedes-ia4sw/mantenedores` para los ficheros en `experiencias/`.
2. El reviewer comprueba: plantilla completa, campos obligatorios, convenciones
   de nombre y disciplinas SWEBOK, y que el contenido sea comprensible y
   replicable por un docente de otra universidad.
3. Los comentarios se hacen directamente sobre el diff del PR. El autor
   responde o aplica los cambios solicitados.
4. Con al menos **una aprobación** de un mantenedor de distinta universidad,
   el PR puede mergearse.
5. El merge se hace con **squash** para mantener el historial de `main` limpio.

El objetivo de la revisión es constructivo: mejorar la claridad y replicabilidad
de la experiencia, no filtrar aportaciones. Cualquier experiencia bien documentada
tiene cabida en el repositorio.

---

## Preguntas frecuentes

**¿Puedo documentar una experiencia que no salió como esperaba?**
Sí, y es especialmente valioso. Las secciones de análisis crítico y lecciones
aprendidas son las más útiles para otros docentes.

**¿Puedo actualizar una experiencia ya publicada?**
Sí. Abre un PR con los cambios y explica en la descripción qué ha cambiado y por qué.

**¿Puedo documentar la misma herramienta que otra experiencia existente?**
Sí, siempre que el contexto sea diferente (asignatura, metodología, nivel educativo).
La diversidad de contextos es precisamente el valor del repositorio.

**¿Es necesario tener datos cuantitativos en la sección de resultados?**
No es obligatorio, pero sí recomendable. Evidencias cualitativas (reflexiones,
citas de estudiantes, observaciones del docente) también son válidas.

**¿Quién puede ser mantenedor?**
Cualquier docente que haya contribuido al menos una experiencia publicada y
quiera implicarse en la revisión. Abre un Issue con la etiqueta `mantenedor`
para solicitarlo.