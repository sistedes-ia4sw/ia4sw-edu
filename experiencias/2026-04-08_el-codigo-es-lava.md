---
creada: 2026-04-08
titulo: El código es lava
universidad: Universidad de Alicante
autores: Cristina Cachero
asignatura: Gestión de Calidad Software
tipo_experiencia: Taller
estado: En desarrollo
curso: 4
cuatrimestre: C2
estudiantes: 80
fecha_academica: 2026-03-27
url: -"
tags:
  - Maintenance
  - Quality

---

# El código es lava
## 1. Información General

### Descripción General
La innovación “El código es lava” tiene como propósito que el estudiantado experimente un paradigma de desarrollo impulsado por IA en el que su rol principal no es “picar código”, sino diseñar, especificar y verificar cambios en un sistema software existente, usando el framework OpenSpec como eje conductor. La idea central es que el código se convierte en “lava”: intocable directamente, de modo que cualquier cambio debe pasar por buenas especificaciones y por la mediación de un agente IA.

### Motivación
En la era de la IA es fundamental que el alumnado aprenda a evaluar la calidad del código generado por la IA. Además, es importante que adquiera habilidades para poder influir en esa calidad a través de las especificaciones.

### Experiencias relacionadas

<!-- Enlaza y comenta otras experiencias relacionadas -->

---

## 2. Objetivos de la Innovación

### Conocimientos (saber)
- Explicar el rol de la IA generativa y de OpenSpec en un flujo de desarrollo de software basado en especificaciones (Spec-Driven  Development).
- Reconocer las limitaciones y riesgos de delegar la escritura de código en un LLM (alucinaciones, errores de lógica, problemas de seguridad, deuda técnica, etc.).

### Habilidades procedimentales (saber hacer)
- Formular una nueva funcionalidad como historia de usuario y criterios de aceptación, asegurando claridad funcional y técnica.
- Redactar especificaciones OpenSpec de calidad, que:
	- Delimiten alcance y no alcance de la modificación.
	- Hagan explícitas las restricciones de arquitectura, estilo de código y pruebas.
	- Incluyan criterios de éxito verificables.
- Orquestar modificaciones de código mediante OpenSpec, de forma que el cambio:
	- Afecte coherentemente a backend, frontend y base de datos.
	- Mantenga la integridad y el comportamiento previo de la aplicación.
- Revisar y evaluar el código generado por la IA, proponiendo mejoras o correcciones cuando la solución no cumple las especificaciones o introduce problemas.

### Competencias actitudinales y metacognitivas (saber ser)
- Adoptar una actitud crítica frente a las respuestas de la IA, evitando la aceptación automática y desarrollando criterios propios de calidad.
- Reflexionar sobre la experiencia de desarrollo “sin tocar el código”, identificando ventajas, limitaciones y posibles escenarios de aplicación/abuso en el contexto profesional.

---

## 3. Metodología y Diseño

### Estrategia Didáctica
- Aprendizaje basado en proyectos (ABP): el proyecto consiste en extender una aplicación existente con una nueva funcionalidad transversal.
- Aprendizaje experiencial: el estudiantado vive en primera persona la experiencia de “no tocar código” y tener que confiar —condicionalmente— en la IA.
- Constructive alignment: la secuencia de actividades está alineada con los objetivos descritos (formulación de requisitos, creación de specs, ejecución asistida por IA, verificación y reflexión final).

### Recursos y Herramientas
- Cuenta github del alumnado
- IDE antigravity (con agente IA integrado). 
- Docker y OpenSpec instalado en el entorno. 
- Repositorio inicial en GitHub con:
	- Aplicación sencilla pero completa dockerizada (frontend + backend + BD) funcionando.
	- Documentación mínima (README, diagrama de arquitectura de alto nivel, endpoints principales, esquema de BD).

### Secuencia de Actividades Formativas
1. Introducción y contexto (15–20 minutos)

El profesorado presenta:

- El título y la metáfora: “El código es lava”.
- El contexto: impacto de la IA generativa en el desarrollo de software.
- Los objetivos del taller y las reglas clave (especialmente: no tocar código manualmente).

El profesorado realiza una breve demo del repositorio inicial y explicación de la arquitectura general (frontend, backend, BD).

2. Exploración guiada de la aplicación existente (15–20 minutos)

De manera individual, cada estudiantes:
- Levanta la aplicación (por ejemplo, docker compose up o comando equivalente).
- Navega por la interfaz y anota funcionalidades actuales.
- Identifica qué tipos de datos existen y cómo se relacionan (a partir de la BD, el código de backend y el asistente de código integrado en el IDE)

El profesorado plantea preguntas guía:
- “¿Dónde creéis que habría que tocar para añadir X?”
- “¿Qué riesgos veis si la IA tocara esta parte sin restricciones claras?”

3. Definición de la nueva funcionalidad (20–25 minutos)
- Cada estudiante recibe un enunciado base de funcionalidad (común) o se le permite elegir entre varias opciones.
- El grupo formula:
-- 1–2 historias de usuario (formato “Como [rol] quiero [acción] para [beneficio]”).
-- Un conjunto de criterios de aceptación verificables.
- Se contrastan ejemplos en la clase para asegurar un mínimo de calidad y realismo.

4. Introducción al framework OpenSpec y a la “escritura de specs” (15–20 minutos)

El profesorado explica brevemente:
- Qué es OpenSpec y cómo se estructura una spec típica (contexto, restricciones, pasos, criterios de éxito).
- El flujo de trabajo general: especificar → ejecutar agente IA → revisar código → probar.

El profesorado realiza una demostración rápida de cómo una spec bien redactada se traduce en cambios de código coherentes (ejemplo muy sencillo).

5. Redacción colaborativa de especificaciones OpenSpec (30–40 minutos)

En grupos, el estudiantado redacta la spec para su funcionalidad, teniendo en cuenta:
- El impacto en frontend, backend y BD.
- Las restricciones de arquitectura, estilo y pruebas definidas por la asignatura.
- Los criterios de aceptación definidos previamente.

El profesorado circula entre grupos, realizando micro-coaching:
- Afinar requisitos difusos.
- Señalar ausencias importantes (p. ej., casos de error, validaciones).
- Recordar la necesidad de pensar en pruebas.

6. Ejecución del flujo OpenSpec + IA y revisión de cambios (30–40 minutos)
Cada alumno:
- Lanza el workflow OpenSpec correspondiente a su spec.
- Inspecciona los cambios propuestos en el código (diffs en GitHub o local).

Evalúa:
- ¿Se han tocado las capas esperadas?
- ¿Se cumplen los criterios de aceptación?
- ¿Se ha roto alguna funcionalidad previa?

Si es necesario, ajusta la spec y reitera el flujo.

Se enfatiza que el producto final no es sólo “que funcione”, sino cómo se ha guiado a la IA para llegar a esa solución.

7. Pruebas funcionales y mini–retrospectiva en grupo (20–25 minutos)

Cada alumno:
- Despliega la aplicación con la nueva funcionalidad y la prueba.
- Registra incidencias, decisiones y trade-offs.
- Responde brevemente (en un formulario o documento compartido) a cuestiones como:
-- ¿Qué parte ha sido más difícil: especificar o revisar?
-- ¿En qué ha sido útil la IA? ¿En qué ha sido problemática?

8. Puesta en común y reflexión final (15–20 minutos)

Discusión plenaria guiada por el profesorado:
- ¿Qué cambiarían en su forma de trabajar con IA después de este taller?
- ¿Qué implicaciones tiene esto para el rol del ingeniero/a de software?
- ¿Qué riesgos ven en delegar “demasiado” en la IA?

Conclusión conectando con la asignatura:
- Cómo encaja este enfoque con el tema de calidad software

### Rol del Profesor
- Diseñador/a del escenario: define la app base y la nueva funcionalidad “tipo” (p. ej., un nuevo módulo de gestión de comentarios, un sistema de favoritos, o un filtro avanzado que requiere cambios en la BD).
- Facilitador/a y coach: guía al alumnado en la formulación de requisitos y en el diseño de especificaciones, interviniendo sólo cuando se bloquean o se desvían de los objetivos.
- “Guardian de la lava”: vela porque nadie modifique el código a mano y todo cambio pase por el flujo OpenSpec + IA.
- Moderador/a de la reflexión final: ayuda a conectar la experiencia con la realidad profesional y con los contenidos de la asignatura.

### Rol del Estudiantado
- Analiza el sistema existente, identificando qué partes se verán afectadas por la nueva funcionalidad.
- Formula la funcionalidad en términos de historias de usuario y criterios de aceptación, negociando el alcance dentro del grupo.
- Redacta y refina las especificaciones OpenSpec, ajustándolas iterativamente en función de los resultados generados por la IA.
- Ejecuta el workflow OpenSpec, revisa los cambios en el repo y se encarga de comprobar que la app sigue funcionando y de validar que la nueva funcionalidad cumple lo especificado.
- Documenta la experiencia, recogiendo problemas, decisiones de diseño y aprendizajes.

### Consideraciones Metodológicas Adicionales

<!-- Otras consideraciones metodológicas relevantes -->

---

## 4. Implementación y Resultados

### Ejecución en el Aula

<!-- Describe cómo se llevó a cabo la experiencia con los estudiantes -->

### Participación e Involucramiento

<!-- ¿Cuál fue el nivel de participación de los alumnos? -->

### Resultados Observados

<!-- Presenta los resultados obtenidos y evidencias recolectadas -->

### Datos de Evaluación

<!-- Rendimiento de estudiantes, datos de evaluación, encuestas... -->

---

## 5. Análisis Crítico y Reflexión

### Análisis Evaluativo

<!-- Valora en qué medida se cumplieron los objetivos, aciertos y fortalezas -->

### Desafíos y Obstáculos

<!-- ¿Qué dificultades encontraste y cómo las abordaste? -->

### Consideraciones Éticas

<!-- Implicaciones éticas del uso de IA (privacidad, sesgos, honestidad académica) -->

### Lecciones Aprendidas

<!-- Reflexiona sobre el impacto en tu práctica docente -->

---

## 6. Guía de Replicabilidad

### Guía de Implementación

<!-- Orientaciones prácticas para replicar esta innovación -->

### Requisitos Previos

<!-- Conocimientos de IA, infraestructura, preparación del alumnado... -->

### Elementos Clave

<!-- ¿Qué no debe omitirse para asegurar el éxito? -->

---

## 7. Futuras Mejoras o Adaptaciones

### Mejoras Propuestas
- Las explicaciones del profesorado sobre OpenSpec podrían grabarse en vídeo para poder ser reutilizadas por docentes que tengan menos experiencia. 
- La experiencia podría venir acompañada de unas transparencias que ayudaran al profesor a presentar la actividad

### Adaptaciones a Otros Contextos
- Posibles extensiones (p. ej., introducir métricas, seguridad, refactorizaciones dirigidas por IA, etc.).
- Trabajo grupal en lugar de trabajo individual