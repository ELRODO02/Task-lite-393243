# SPEC-000 — Fundación de TaskFlow Lite

## 1. Propósito

Establecer la base técnica inicial de **TaskFlow Lite** sobre la cual se desarrollarán posteriormente las capacidades funcionales del producto.

Esta especificación define la estructura mínima del proyecto, tecnologías permitidas, restricciones técnicas, convenciones de desarrollo y criterios técnicos de finalización.

En esta etapa **no se implementarán historias de usuario ni funcionalidades relacionadas con la gestión de tareas**.

---

## 2. Alcance

Esta SPEC contempla únicamente la preparación inicial del proyecto TaskFlow Lite.

Incluye:

- Definición de la estructura base del proyecto.
- Uso de HTML5, CSS3 y JavaScript mediante ES Modules.
- Organización del código fuente dentro de `src/`.
- Preparación para ejecutar el proyecto localmente desde VS Code.
- Definición de convenciones básicas de nombres.
- Definición de convenciones iniciales de Git.
- Preparación del proyecto para utilizar `localStorage` en futuras funcionalidades.
- Establecimiento de una Definition of Done técnica inicial.

La finalidad de esta SPEC es contar con una base consistente antes de comenzar el desarrollo funcional.

---

## 3. Estructura inicial del proyecto

La estructura inicial esperada será:

```text
taskflow-lite/
│
├── src/
│   ├── css/
│   ├── js/
│   └── index.html
│
├── specs/
│   └── SPEC-000-foundation.md
│
├── .gitignore
└── README.md
```

Responsabilidad inicial de cada elemento:

- `src/`: contiene el código fuente ejecutable de la aplicación.
- `src/index.html`: punto de entrada de TaskFlow Lite.
- `src/css/`: contiene los archivos de estilos CSS.
- `src/js/`: contiene los módulos JavaScript.
- `specs/`: contiene las especificaciones del proyecto.
- `.gitignore`: define archivos o directorios que no deben versionarse.
- `README.md`: contiene información básica para identificar y ejecutar el proyecto.

La creación de carpetas adicionales deberá responder a una necesidad concreta establecida en una SPEC posterior.

---

## 4. Restricciones técnicas

El proyecto deberá respetar las siguientes restricciones:

- Utilizar **HTML5** para la estructura de la interfaz.
- Utilizar **CSS3** para presentación y estilos.
- Utilizar **JavaScript moderno mediante ES Modules**.
- No utilizar frameworks de frontend.
- No utilizar frameworks de CSS.
- No utilizar backend.
- No depender de una base de datos externa.
- La futura persistencia de datos se realizará mediante `localStorage`.
- No implementar todavía persistencia funcional.
- Todo el código fuente de la aplicación deberá mantenerse dentro de `src/`.
- El proyecto deberá poder ejecutarse localmente desde VS Code mediante un servidor estático local compatible con ES Modules.
- No incorporar dependencias externas salvo que una SPEC posterior las autorice explícitamente.
- No implementar funcionalidades que no estén definidas previamente en una SPEC aprobada.

---

## 5. Convenciones de nombres

Se utilizarán las siguientes convenciones iniciales:

### Archivos y carpetas

Los nombres deberán:

- Escribirse en minúsculas.
- Utilizar palabras descriptivas.
- Utilizar `kebab-case` cuando el nombre contenga varias palabras.

Ejemplos:

```text
task-list.js
task-form.js
main-content.css
```

### JavaScript

Para variables y funciones se utilizará `camelCase`.

Ejemplos:

```text
taskList
currentTask
renderTasks
saveTask
```

Las constantes cuyo valor sea considerado global e inmutable podrán utilizar `UPPER_SNAKE_CASE`.

Ejemplo:

```text
STORAGE_KEY
```

### CSS

Las clases CSS utilizarán nombres descriptivos en `kebab-case`.

Ejemplos:

```text
.task-card
.task-list
.main-header
```

Los nombres deberán describir el propósito del elemento y evitar referencias innecesarias a detalles visuales que puedan cambiar.

---

## 6. Convenciones de Git

El repositorio utilizará Git para mantener el historial del proyecto.

Las ramas principales serán:

- `main`: versión estable del proyecto.
- `develop`: integración del trabajo en desarrollo.

Cuando sea necesario desarrollar una capacidad independiente, podrán utilizarse ramas de trabajo con el siguiente formato:

```text
feature/nombre-capacidad
```

Para trabajo técnico que no represente una funcionalidad:

```text
chore/nombre-cambio
```

Para correcciones:

```text
fix/nombre-correccion
```

Los mensajes de commit deberán ser breves y describir claramente el cambio realizado.

Formato recomendado:

```text
tipo: descripción
```

Ejemplos:

```text
chore: crear estructura inicial del proyecto
docs: agregar spec de fundación
fix: corregir ruta del módulo principal
```

No se deberán mezclar cambios no relacionados dentro de un mismo commit cuando puedan separarse razonablemente.

---

## 7. Definition of Done técnica inicial

La SPEC-000 se considerará técnicamente completada cuando:

- La estructura inicial definida en esta SPEC exista.
- El código fuente se encuentre dentro de `src/`.
- El proyecto pueda abrirse correctamente desde VS Code.
- La página inicial pueda cargarse mediante un servidor estático local.
- El navegador pueda interpretar correctamente los ES Modules del proyecto.
- No existan errores de carga relacionados con archivos o rutas de la estructura inicial.
- No se hayan agregado frameworks ni backend.
- No se hayan implementado historias funcionales.
- El repositorio Git contenga únicamente archivos necesarios para el proyecto.
- Los nombres de archivos y carpetas respeten las convenciones establecidas.
- Los cambios correspondientes a la fundación estén versionados mediante Git.
- `SPEC-000-foundation.md` forme parte del repositorio como referencia técnica inicial.

---

## 8. Fuera de alcance

Esta SPEC no contempla:

- Crear tareas.
- Visualizar listas de tareas.
- Actualizar tareas.
- Editar tareas.
- Eliminar tareas.
- Cambiar estados de tareas.
- Filtrar tareas.
- Implementar `localStorage`.
- Definir el modelo definitivo de una tarea.
- Diseñar el flujo funcional de la aplicación.
- Implementar autenticación.
- Implementar usuarios o equipos.
- Implementar backend.
- Implementar APIs.
- Implementar bases de datos.
- Incorporar frameworks o librerías externas.
- Desarrollar historias de usuario.
- Definir funcionalidades futuras que todavía no hayan sido especificadas.

Cualquier funcionalidad posterior deberá definirse mediante una nueva SPEC antes de su implementación.