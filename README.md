# Base de Conocimiento de Experiencias Docentes con IA en Ingeniería del Software

Repositorio colaborativo que recopila experiencias de uso de **Inteligencia Artificial Generativa** en la docencia de asignaturas de **Ingeniería del Software**. Está mantenido por docentes de múltiples universidades con el objetivo de compartir, documentar y facilitar la replicabilidad de innovaciones pedagógicas.

## ¿Qué contiene este repositorio?

Cada experiencia es un fichero Markdown (`.md`) que documenta de forma estructurada cómo un docente ha integrado herramientas de IA generativa en su asignatura. Las experiencias siguen una plantilla común con siete secciones:

1. **Información General** — Datos básicos: universidad, asignatura, curso, disciplinas SWEBOK implicadas.
2. **Objetivos de la Innovación** — Qué conocimientos, habilidades y competencias se persiguen.
3. **Metodología y Diseño** — Estrategia didáctica, herramientas, secuencia de actividades, roles.
4. **Implementación y Resultados** — Ejecución en el aula, participación, evidencias y datos.
5. **Análisis Crítico y Reflexión** — Evaluación, desafíos, ética y lecciones aprendidas.
6. **Guía de Replicabilidad** — Orientaciones prácticas para que otros docentes puedan reproducir la experiencia.
7. **Futuras Mejoras o Adaptaciones** — Propuestas de evolución y transferencia a otros contextos.

## Estructura del repositorio

```
.
├── README.md                   # Este fichero
├── CONTRIBUTING.md             # Guía detallada de contribución
├── LICENSE
├── plantillas/
│   └── experiencia.md    # Plantilla Templater para Obsidian
├── experiencias/
│   ├── chatgpt-generacion-casos-prueba.md
│   ├── copilot-pair-programming-construccion.md
│   └── ...
└── assets/           # Imágenes y recursos referenciados desde las experiencias
    └── img/
```

## Cómo consultar la base de conocimiento

### En GitHub (navegador)

Navega a la carpeta [`experiencias/`](experiencias/) y abre cualquier fichero `.md`. GitHub renderiza el Markdown directamente, incluyendo el frontmatter YAML como tabla de metadatos. Puedes usar la búsqueda de GitHub (`/` o la barra de búsqueda) para localizar experiencias por universidad, herramienta, disciplina SWEBOK, etc.

### En Obsidian (local)

1. Clona el repositorio:
   ```bash
   git clone https://github.com/TU-ORG/ai-se-learn.git
   ```
2. Abre la carpeta clonada como vault en Obsidian (*Open folder as vault*).
3. Abre el fichero listado (BASE) que contiene un listado interactivo de todas las experiencias que permite aplicar filtros por cualquiera de los datos de la información general, como por ejemplo el nombre de una universidad.
4. Si instalas el plugin **Templater** y configuras `_templates/` como carpeta de plantillas, podrás crear nuevas experiencias de forma guiada.

### Plugins de Obsidian recomendados

| Plugin | Uso |
|--------|-----|
| **Dataview** | Consultas y vistas agregadas sobre las experiencias |
| **Templater** | Creación guiada de nuevas experiencias con la plantilla |
| **Calendar** | Navegación temporal por fecha académica |

## Cómo aportar una experiencia

### Opción A: Pull Request (recomendada para usuarios de Git)

1. Haz **fork** de este repositorio.
2. Crea una rama descriptiva:
   ```bash
   git checkout -b experiencia/tu-universidad-tema-breve
   ```
3. Copia la plantilla y rellénala:
   ```bash
   cp _templates/"Experiencia IA-IS.md" experiencias/titulo-de-tu-experiencia.md
   ```
   Rellena el frontmatter YAML y todas las secciones. Consulta la [guía de contribución](CONTRIBUTING.md) para los detalles sobre convenciones de nombres, campos obligatorios y estilo.
4. Haz **commit** y **push**:
   ```bash
   git add experiencias/titulo-de-tu-experiencia.md
   git commit -m "Nueva experiencia: Título de tu experiencia"
   git push origin experiencia/tu-universidad-tema-breve
   ```
5. Abre un **Pull Request** contra la rama `main`. Un mantenedor revisará tu contribución y te proporcionará feedback si es necesario.

### Opción B: Issue (para quienes no usen Git habitualmente)

Si no estás familiarizado con el flujo de Pull Requests, puedes aportar tu experiencia abriendo un **Issue** con la etiqueta `nueva-experiencia`. Usa la plantilla de Issue proporcionada, que contiene los mismos campos que la plantilla Markdown. Un mantenedor se encargará de convertirlo en el fichero `.md` correspondiente y te dará crédito como autor.
<!--
➡️ [Abrir un Issue de nueva experiencia](../../issues/new?template=nueva-experiencia.yml&labels=nueva-experiencia)
-->
## Convenciones

### Nombres de fichero

Usa kebab-case descriptivo basado en el tema principal de la experiencia:

```
chatgpt-generacion-casos-prueba.md
copilot-pair-programming-construccion.md
claude-revision-codigo-arquitectura.md
```

### Campos obligatorios del frontmatter

Los campos marcados con `*` en la plantilla son obligatorios: `titulo`, `universidad`, `autores`, `asignatura`, `estado` y `curso`. El resto son opcionales pero muy recomendables para maximizar la utilidad de la base de conocimiento.

### Disciplinas SWEBOK

Usa exactamente estos valores en el campo `disciplinas_swebok` para garantizar la consistencia en las búsquedas:

`Requirements` · `Architecture` · `Design` · `Construction` · `Testing` · `Operations` · `Maintenance` · `Configuration Management` · `Management` · `Process` · `Models and Methods` · `Quality` · `Security`

### Idioma

Las experiencias pueden redactarse en **español** o en **inglés**. El frontmatter YAML debe mantener los nombres de campo en español tal como están definidos en la plantilla para garantizar la compatibilidad con las consultas Dataview.

### Imágenes y recursos

Si tu experiencia incluye imágenes, diagramas u otros recursos, colócalos en `assets/img/` con un prefijo que identifique tu experiencia (por ejemplo, `assets/img/chatgpt-casos-prueba-diagrama.png`) y referenciarlos con rutas relativas:

```markdown
![Diagrama del flujo de trabajo](../assets/img/chatgpt-casos-prueba-diagrama.png)
```

## Gobernanza y revisión

Este repositorio se gestiona con un modelo abierto de revisión por pares:

- **Mantenedores**: un grupo de docentes de distintas universidades con permisos de merge. Si quieres unirte como mantenedor, abre un Issue con la etiqueta `mantenedor`.
- **Revisión de PRs**: cada PR es revisado por al menos un mantenedor que no sea de la misma universidad que el autor, para garantizar que la experiencia es comprensible y replicable por terceros.
- **Criterios de aceptación**: la experiencia debe usar la plantilla oficial, tener los campos obligatorios completos, y aportar contenido sustancial en al menos las secciones 1–4.

## Código de conducta

Este es un espacio académico y profesional. Se espera que todas las interacciones (Issues, PRs, comentarios) mantengan un tono respetuoso y constructivo. Nos adherimos al [Contributor Covenant v2.1](https://www.contributor-covenant.org/es/version/2/1/code_of_conduct/).

## Licencia

El contenido de este repositorio se distribuye bajo licencia [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/deed.es). Puedes reutilizar y adaptar las experiencias siempre que cites la autoría original y mantengas la misma licencia.

## Contacto

Si tienes dudas sobre el proyecto o quieres proponer mejoras en la estructura de la base de conocimiento, abre un [Issue de discusión](../../issues/new?labels=discusión) o contacta con los mantenedores.