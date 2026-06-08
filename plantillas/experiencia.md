---
<%*
const titulo = await tp.system.prompt("Título del Proyecto");
const universidad = await tp.system.prompt("Universidad");
const autores= await tp.system.prompt("Profesor(es) / Autores (separados por coma)"); 
const asignatura = await tp.system.prompt("Asignatura");
const tipo_experiencia = await tp.system.suggester(["Actividad", "Caso de Estudio", "Taller", "Proyecto", "Laboratorio"], ["Actividad", "Caso de Estudio", "Taller", "Proyecto", "Laboratorio"]);
const estado = await tp.system.suggester(["Activa", "En desarrollo", "Archivada"], ["Activa", "En desarrollo", "Archivada"]);
const curso = await tp.system.suggester(["1º", "2º", "3º", "4º", "Máster"], ["1", "2", "3", "4", "Master"]);
const cuatrimestre = await tp.system.suggester(["Primer cuatrimestre", "Segundo cuatrimestre", "Anual"], ["C1", "C2", "Anual"]);
const estudiantes = await tp.system.prompt("Número de estudiantes");
const url = await tp.system.prompt("URL de información adicional (dejar vacío si no hay)","-");

const kebab = titulo
  .normalize("NFD").replace(/[\u0300-\u036f]/g, "")
  .toLowerCase()
  .replace(/[^a-z0-9\s-]/g, "")
  .trim()
  .replace(/\s+/g, "-");
const nombre = tp.date.now("YYYY-MM-DD") + "_" + kebab;
await tp.file.rename(nombre);
await tp.file.move("/experiencias/" + nombre);
%>
creada: <% tp.date.now("YYYY-MM-DD") %> 
titulo: <% titulo %>
universidad: <% universidad %>
autores: <% autores %>
asignatura: <% asignatura %>
tipo_experiencia: <% tipo_experiencia %>
estado: <% estado %>
curso: <% curso %>
cuatrimestre: <% cuatrimestre %>
estudiantes: <% estudiantes %>
fecha_academica: <% tp.date.now("YYYY-MM-DD") %> 
url: <% url %>" 
tags:
  - Requirements
  - Architecture
  - Design
  - Construction
  - Testing
  - Operations
  - Maintenance
  - Configuration_Management
  - Management
  - Process
  - Models_and_Methods
  - Quality
  - Security

---

# <% titulo %>
## 1. Información General

### Descripción General

<!-- Introduce una descripción general de la actividad -->

### Motivación

<!-- ¿Por qué crees que esta experiencia es relevante para la asignatura? -->

### Experiencias relacionadas

<!-- Enlaza y comenta otras experiencias relacionadas -->

---

## 2. Objetivos de la Innovación

### Conocimientos (saber)

<!-- Describe los conocimientos específicos que se pretenden desarrollar -->

### Habilidades procedimentales (saber hacer)

<!-- ¿Qué habilidades prácticas se pretenden desarrollar? -->

### Competencias actitudinales y metacognitivas (saber ser)

<!-- ¿Qué competencias actitudinales y de reflexión se pretenden desarrollar? -->

---

## 3. Metodología y Diseño

### Estrategia Didáctica

<!-- Explica el enfoque pedagógico adoptado -->

### Recursos y Herramientas

<!-- Describe las herramientas de IA, plataformas y recursos necesarios -->

### Secuencia de Actividades Formativas

<!-- Paso 1: ... Paso 2: ... Paso 3: ... -->

### Rol del Profesor

<!-- Describe el rol y las funciones del profesor -->

### Rol del Estudiantado

<!-- Describe el rol y las funciones de los estudiantes -->

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

<!-- ¿Cómo se podría optimizar o ampliar la experiencia? -->

### Adaptaciones a Otros Contextos

<!-- ¿Cómo podría adaptarse a otras asignaturas o niveles? -->