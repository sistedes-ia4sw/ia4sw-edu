---
creada: 2026-04-08
titulo: "Del ‘Ship it’ al ‘Prove it’: Auditoría de Calidad con y sin IA"
universidad: Universidad de Alicante
autores: Cristina Cachero
asignatura: Gestión de Calidad Software
tipo_experiencia: Actividad
estado: En desarrollo
curso: 1
cuatrimestre: C1
estudiantes: 80
fecha_academica: 2025-12-15
url:
tags:
  - Quality
---

# Del ‘Ship it’ al ‘Prove it’: Auditoría de Calidad con y sin IA
## 1. Información General

### Descripción General
En grupos de 3, el estudiantado construye en casa una app full-stack sencilla con Lovable y la sincroniza con GitHub; después, cada integrante realiza una evaluación individual del mismo código con un método distinto (manual “a su manera” sin IA, con IA “a su manera”, y con tus prompts guiados), documentando hallazgos con evidencias; en clase (2h) el grupo consolida un informe único de calidad que atribuye qué método aportó cada problema y por qué, y se cierra con 30 minutos de debate comparativo.

### Motivación
Esta experiencia entrena una habilidad “de senior”: detectar y argumentar problemas de calidad (no solo “que funcione”), y además desarrolla criterio para usar IA con cabeza: cuándo acelera el análisis, cuándo introduce ruido o sesgos, y cómo diseñar prompts/procesos que aumenten la fiabilidad del juicio técnico. En 4º curso, esto conecta muy bien con la transición a prácticas profesionales y al rol de revisor/a responsable.

### Experiencias relacionadas

<!-- Enlaza y comenta otras experiencias relacionadas -->

---

## 2. Objetivos de la Innovación

### Conocimientos (saber)
Modelo de calidad de producto (por ejemplo ISO/IEC 25010 para hablar con un vocabulario compartido de “qué es calidad” más allá de gustos personales), nociones de mantenibilidad, fiabilidad, seguridad, usabilidad y rendimiento; fundamentos de control de versiones y trazabilidad en GitHub; y principios básicos de seguridad en SDLC (p. ej., prácticas del NIST SSDF como revisar temprano y usar análisis para encontrar issues de seguridad).

### Habilidades procedimentales (saber hacer)
Levantar un checklist/rúbrica de revisión; inspeccionar un repo y localizar evidencia (archivos, funciones, rutas); clasificar hallazgos por severidad e impacto; redactar issues accionables (“qué pasa, dónde, por qué importa, cómo mitigarlo”); usar IA como “copiloto de revisión” sin delegar el juicio (hacer preguntas, pedir contraejemplos, solicitar pruebas, detectar alucinaciones); y fusionar hallazgos en un informe con trazabilidad y atribución de contribuciones.

### Competencias actitudinales y metacognitivas (saber ser)
Humildad epistémica (no confundir confianza con certeza, especialmente con IA), ética profesional (no exponer secretos ni datos), responsabilidad sobre seguridad y calidad, colaboración y negociación de criterios dentro del grupo, y calibración de confianza (cuándo aceptar/rechazar una sugerencia de IA y cómo justificarlo).

---

## 3. Metodología y Diseño

### Estrategia Didáctica
Aprendizaje basado en producto + evaluación comparativa de métodos + deliberación estructurada. La comparación “tres miradas” dentro del mismo equipo crea un micro-experimento controlado (mismo código, tres procesos), y el cierre tipo controversia/consenso favorece pensamiento crítico (no “ganar” sino entender trade-offs).

### Recursos y Herramientas
Lovable para construir y sincronizar con GitHub (integración oficial) ; GitHub (repo, issues/PRs si queréis); Antigravity conectado al repo como entorno de navegación y, para dos roles, como apoyo con IA agente (con controles de seguridad y aprobaciones) ; y opcionales: linters/tests del stack (p. ej., ESLint/TypeScript, pruebas unitarias/e2e) y un marco de criterios tipo ISO/IEC 25010 para etiquetar hallazgos.. Prompts guiados (para tu tercer rol), listos para copiar (adaptan frontend/back y obligan a evidencias):

### Secuencia de Actividades Formativas
Casa, equipo: 
1. elegir un “scope común” de app que tú fijas con 2–3 requisitos (30 min); 
2. construir con Lovable y dejar la app funcional (2–3 h); 
3. sincronizar con GitHub y crear un tag “v1.0-review” para congelar el estado a revisar (15 min) 

Casa, individual: 
4. Revisor/a A (sin IA): revisa el repo y documenta hallazgos con evidencia (2–3 h); 
5. Revisor/a B (IA libre): usa IA como quiera, pero debe guardar “diario de uso” (prompts, tiempo, decisiones) y producir hallazgos con evidencia (2–3 h); 
6. Revisor/a C (IA guiada): usa tus prompts y el mismo formato de reporte (2–3 h); 

Clase, 2h: 
7. reunión de tríada: fusionan listas, eliminan duplicados, resuelven discrepancias y crean informe final atribuyendo “este issue lo detectó A/B/C y así influyó” (90 min); 
8. “calibración final”: el grupo marca 3 hallazgos donde la IA fue especialmente útil y 3 donde fue engañosa o poco fiable, con justificación (30 min); 

Clase, 30 min:
9. debate: patrones globales (qué categorías detecta mejor cada método, qué sesgos aparecen, y qué proceso híbrido recomendaríais). 

Para gestionar 80 personas, funciona muy bien cerrar con “top-3 hallazgos por grupo” en pizarra compartida y discutir por clústeres (seguridad, mantenibilidad, UX/performance).

### Rol del Profesor
Diseñar el “scope común” para que los repos sean comparables; entregar la plantilla de reporte (campos obligatorios: evidencia, severidad, categoría ISO 25010, recomendación); enseñar 10 minutos de “cómo escribir un issue accionable”; marcar reglas de uso de IA (transparencia, diario, no inventar evidencias); y moderar el debate para que no sea “IA sí/no”, sino “en qué condiciones y con qué proceso aporta valor”.

### Rol del Estudiantado
Construir en equipo con disciplina mínima (commits comprensibles, tag de freeze), realizar revisión individual rigurosa (con o sin IA según rol) y defender hallazgos con evidencia; en la síntesis, negociar criterios, priorizar impacto y producir un informe final que sea útil para “quien mantiene el sistema”, no solo para aprobar.

### Consideraciones Metodológicas Adicionales

- Para que el experimento sea justo, fija un corte temporal (tag) y prohíbe cambios posteriores hasta terminar revisiones; exige “evidencia o no cuenta” (evita alucinaciones); y, si se usa Antigravity en modo agente, configura aprobación explícita para comandos/acciones (mejor “read-only review”) y evita repos con secretos, porque herramientas agentivas con terminal pueden introducir riesgos si tienen demasiada autonomía. 
- Obliga a cada rol a incluir (a) 2 hallazgos “en los que podría estar equivocado/a” y cómo los verificaría; (b) 1 hallazgo donde cambió de opinión tras buscar evidencia; y (c) un “contraargumento” por cada hallazgo severo (qué defensa podría dar quien escribió el código). Además, en el debate pide que la clase diseñe un “proceso híbrido mínimo viable” (qué pasos humanos son irrenunciables y dónde la IA aporta más).

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

Añadir una fase corta de “fix & PR”: cada grupo abre 3 PRs (uno por dimensión: seguridad, mantenibilidad, UX/performance) y re-ejecuta la revisión para ver qué método detecta regresiones; incorporar métricas automáticas (coverage, lint, análisis estático) como “tercer tipo de evidencia”; o repetir el estudio con otra herramienta de generación para comparar generalización.

### Adaptaciones a Otros Contextos

En un máster/empresa, convertirlo en una práctica de política de calidad: definir un “Definition of Done” con ISO 25010 + prácticas SSDF y automatizar checks; en bootcamps, reducir el scope a frontend-only y centrarte en accesibilidad/usabilidad; en equipos profesionales, hacerlo como “auditoría de PRs con IA” midiendo tiempo-ahorrado vs falsos positivos y estableciendo guardrails.