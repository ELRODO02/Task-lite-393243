Historias de usuario Y criterios 

# HU-001-Crear una tarea 

##Historia de usuario 

Como integrante del eequipo, quiero registrar una nueva tarea con titulo y descripción, para documentar el trabajo que necesito realizar.



## Criterios de aceptación 

### CA-001-Crear Correctamente

Given que el usuario proporciona el titulo válido 

When solicita crear la tarea.

Then la tarea debe agregarse

And debe de iniciar con un  estado pendiente 

#### CA-002 - Titulo obligatorio
Given que el usuario desea crear una tarea
And no proporciona el título
When intenta registrar la tarea 
Then la tarea no debe de ser creada
And debe recibir información indicando que el título es obligatorio

### CA-003 - Lóngitud mínima del título 
Given que el usuario desea crear una tarea 
And proporciona un titulo con menos de 3 caracteres
When intenta registrar la tarea 
Then la tarea no debe de ser creada 
And debe informarse que el título no coumple con la longitud mínima 

### CA-004 - Lóngitud maxima del título 
Given que el usuario desea crear una tarea 
And proporciona un titulo mayor a 80 caracteres
When intenta registrar la tarea 
Then la tarea no debe de ser creada
And debe informarse que el titulo no cumple con la longitud maxima 

### CA-005 - Descripción Opcional
Given que el usuario proporciona un título válido
And no proporciona descripción 
When registra la tarea 
Then la tarea debe de crearse correctamente 

### CA-006 - Descripción demasiado extensa 
Given que el usuario proporciona una descripción mayor a 300 caractéres
When intenta crear la tarea 
Then la tarea no debe ser registrada
And debe informarse la restricción correspondiente 

## Reglas del negocio 
RN-001: Toda tarea debe de tener título.
Rn-002: El título debe de contener entre 3 y 80 caractéres
RN-003: La descripción es opcional.
RN-004: La descripción tendrá maximo 300 caractéres.
RN-005: Toda tarea nueva inicia como pendiente.
RN-006: Cada tarea debe de poder  identificarse de manera unica.
RN-007: Debe conocerse cuando fue creada la tarea.

## Dependencias
Esta historia no depende funcionalmente de otra HU.

## Fuera de Alcance
* Asignar tareas a personas. 
* Fechas limite.
* Prioridades.
* Categorias.
* Archivos adjuntos.
* SubTareas.
* Notificaciones.


