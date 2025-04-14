# Escenario de caso de uso 2

# Solicitar Turno

## Descripción General
Este caso permite al usuario poder solicitar un turno medico en el momento que desee, siempre y cuando haya un turno disponible

## Flujo de eventos
* El usuario ingresa con su cuenta previamente creada.
* El sistema verifica si los datos son correctos.
* El usuario selecciona el apartado de solicitar un turno.
* El sistema muestra los turnos disponibles según una fecha, horario, especialidad y un médico.
* El usuario selecciona la especialidad, fecha, horario y médico.
* El sistema verifica si esta disponible dicha fecha y médico.
* En caso de estar disponible el sistema muestra un mensaje de "Turno Asignado" y le genera un código de seguimiento sobre el turno, en caso de no estar disponible el sistema pedirá que seleccione un horario o fecha diferente.

 # Precondiciones:
 El usuario debe estar registrado.

# Postcondiciones:
Se genera y asigna un turno.

![image](https://github.com/user-attachments/assets/87963d49-b656-4ba2-9ba5-07b59d617096)



