# Principio de Responsabilidad Unica (SRP)

El Principio de Responsabilidad Única (Single Responsibility Principle, SRP) busca garantizar que una clase tenga un único motivo para modificarse. En otras palabras, cada clase debe ocuparse de una sola función o tarea específica, y todos sus métodos deben estar alineados con esa función.

En un sistema para gestionar turnos médicos, es común encontrar módulos que combinan múltiples funciones en un solo componente. Por ejemplo, una parte del sistema podría encargarse simultáneamente de administrar los turnos, verificar la disponibilidad de los médicos, enviar notificaciones a los pacientes y almacenar los datos en la base de datos.

El SRP sugiere dividir estas tareas en componentes separados, de modo que cada uno cumpla con una única función: uno para asignar turnos, otro para validar horarios, otro para gestionar notificaciones, y otro para manejar el almacenamiento de datos.

## Motivacion

Uno de los principales inconvenientes que tenía el sistema de gestión de turnos médicos era que varias partes del programa asumían múltiples tareas simultáneamente. Por ejemplo, una sola unidad del sistema se encargaba de registrar un turno nuevo, verificar si el médico estaba disponible, notificar al paciente y almacenar toda la información en la base de datos. Esta acumulación de responsabilidades en un solo componente provocaba muchos problemas: el código se volvía complejo, los cambios afectaban múltiples funcionalidades y resultaba más difícil detectar y solucionar errores.

Para aplicar el Principio de Responsabilidad Única (SRP), se optó por dividir esas tareas en módulos independientes. Así, se creó una sección encargada únicamente de generar turnos, otra que verifica la disponibilidad, una que gestiona las notificaciones y una última que se dedica al almacenamiento de datos. Gracias a esta separación, cada componente puede ser modificado, corregido o mejorado sin interferir con los demás, lo que mejora el orden general, reduce los errores y facilita el mantenimiento y la escalabilidad del sistema.

**Ejemplo en la vida real:**

Imaginemos a un recepcionista de una clínica que debe hacerlo todo: atender a los pacientes, organizar los turnos, enviar correos, hacer llamadas, registrar cuentas y limpiar el escritorio. Si se cambia la forma de enviar notificaciones, toda su rutina se ve afectada. Además, si comete un error, no es fácil saber en qué tarea sucedió. Ahora bien, si cada función está asignada a una persona diferente (una para atención, otra para agendamiento, otra para comunicaciones y otra para limpieza), el trabajo se vuelve más claro, eficiente y especializado. Cada persona tiene una tarea específica, y cualquier mejora se puede aplicar de forma más controlada.

## Estructura de Clases

