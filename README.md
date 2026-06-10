# Práctica 2

## 🎯 Objetivo del Proyecto
El objetivo principal de esta práctica es implementar y dominar un flujo de trabajo colaborativo profesional mediante Git y GitHub. Se enfoca en la asignación estratégica de roles dentro de un equipo de desarrollo, el despliegue de un proyecto web estructurado, la revisión de código mediante Pull Requests y la resolución controlada de conflictos de fusión (merge conflicts).

---

## 👥 Integrantes y Roles
* **Rodrigo** - **Líder de Proyecto** (Coordinación general, administración del repositorio y revisión/aprobación de código).
* **Estefany** - **Diseñador UI/UX** (Responsable del diseño visual, estilos CSS y maquetación responsiva en la rama correspondiente).
* **Raúl** - **Integrador Git** (Encargado de la gestión de ramas, fusiones de código y la resolución técnica de conflictos).
* **Misael** - **Documentador** (Responsable de la estructura inicial del proyecto, control de calidad y redacción de la documentación técnica).

---

## 🔄 Flujo de Trabajo Usado
Para este proyecto implementamos el modelo **Feature Branch Workflow** (Flujo de trabajo basado en ramas por característica), asegurando que la línea principal de producción se mantuviera siempre estable.

### 1. Arquitectura de Ramas (Brazos)
El repositorio se estructuró con un total de 3 ramas activas:
* **`main`**: El brazo principal. Contiene única y exclusivamente el código completamente estable, testeado y aprobado por el líder.
* **`dev`**: Rama de desarrollo dedicada a la construcción de la estructura lógica y maquetación del esqueleto HTML5.
* **`diseno`**: Rama de desarrollo enfocada de manera exclusiva en los estilos CSS3, la paleta de colores y la experiencia estética del usuario.

### 2. Proceso de Desarrollo y Commits
Cada integrante trabajó en su entorno local dentro de su respectivo "brazo" de trabajo. Se aplicó una política de commits con mensajes claros, semánticos y descriptivos para mantener la trazabilidad del proyecto, por ejemplo:
* `Feat: Crear estructura HTML base del proyecto` (Trabajado en la rama `dev`).
* `Style: Agregar estilos principales y diseño visual` (Trabajado en la rama `diseno`).

### 3. Pull Request y Revisión de Código
Una vez concluida la maquetación base en la rama `dev`, se abrió un **Pull Request (PR)** hacia `main`. 
* **Rodrigo (Líder)** actuó como revisor formal del código (*Reviewer*), inspeccionando que las etiquetas HTML cumplieran con los estándares de usabilidad.
* Tras aprobar los cambios en la plataforma de GitHub, **Raúl (Integrador)** ejecutó la fusión (*Merge*) de forma segura.

### 4. Simulación y Resolución de Conflictos
Para cumplir con el requerimiento de gestión de conflictos, el equipo provocó un choque real en el archivo `index.html`:
1. **Modificación en `main`:** Se actualizó la línea del encabezado principal `<h1>` directamente en la rama principal.
2. **Modificación en `diseno`:** Simultáneamente, se editó **esa misma línea** en la rama de diseño con un texto diferente.
3. **El Conflicto:** Al intentar integrar los cambios de `main` dentro de la rama `diseno` (`git merge main`), Git detuvo la operación de forma automática debido a la colisión de líneas de código.
4. **La Solución:** El equipo analizó ambas propuestas. El integrador abrió el archivo, eliminó manualmente los marcadores de conflicto (`<<<<<<<`, `=======`, `>>>>>>>`) y unificó los criterios de diseño en una versión final limpia. Se guardaron los cambios, se preparó el archivo con `git add` y se cerró el ciclo con el commit: `Merge: Resolver conflicto de títulos entre main y diseno`.
