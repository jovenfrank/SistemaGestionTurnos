# Escenario de caso de uso 5

# Notificacion de turno proximo

## Descripción General
El sistema le envia una notificacion al usuario via mail y SMS para informar que su turno esta cerca

## Flujo de eventos
* El usuario solicita un turno a través del sistema.
* El sistema registra la información del turno con fecha y hora.
* Cuando el turno se encuentra al menos de 24 horas, el sistema detecta automáticamente la proximidad del evento.
* El sistema genera una notificación personalizada.
* El sistema envía la notificación al usuario por correo electrónico o mensaje dentro de la plataforma.
* El usuario recibe la notificación y se prepara para asistir a su turno.

 # Precondiciones:
* El usuario debe haber agendado un turno en el sistema.
* El usuario debe tener una dirección de correo válida registrada.

# Postcondiciones:
* El usuario recibe una notificación con la información de su turno.
* El evento queda registrado en el historial del sistema.
![image](https://github.com/user-attachments/assets/5a7bb614-0ecf-4cff-b4fc-a20f1f2c11f3)

