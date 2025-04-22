> # Escenarios de Casos de Uso

> ## Caso de uso 1 - Registrar un nuevo paciente

> ### Descripcion general
> Este caso de uso permite que un nuevo usuario se registre llenando un formulario con datos personales como DNI, numero telefonico, correo electronico, etc, una vez registrado estos datos seran validados por el personal administrativo para que se eviten cuenta falsas o duplicadas. Una vez creado el usuario tendra acceso a todas las funciones de paciente como pedir turnos, cancelarlos, consultas medicas, ver el historial y recibir notificaciones.

## Flujo de eventos
1.**Accede al registro:**
- El usuario selecciona la opción de "Reistrarme" en la pagina web.

  2.**Solicitud de datos:**
- El sistema muestra un formulario con campos obligatorios.
    
  3.**Ingreso de datos:**
- El usuario completa los campos obligatorios con sus datos personales, nombre, DNI, fecha de nacimiento, teléfono y correo.

  4.**Verificación de duplicados:**
- El sistema comprueba si ya existe un paciente con ese DNI.

  5.**Guardado de información:**
- Si es válido, la información se guarda en la base de datos.
  
  **Confirmación:**
- El sistema muestra un mensaje indicando que el paciente fue registrado con éxito.

  ## Condiciones
  
 **Precondiciones:**
- El paciente debe tener acceso al sistema.
 
 **Postcondiciones:**
- El paciente queda registrado y podrá gestionar turnos.

* [Enlace del Escenario](https://drive.google.com/file/d/1djVqFc39Qv1jn71jZxvAYOAucAsL_iJs/view?usp=sharing)

## Caso de uso 2 - Iniciar sesion al sistema

### Descripcion general
Permite que los usuarios accedan a su cuenta dentro del sistema según sus credenciales. Cada tipo de usuario (paciente, médico o administrador) verá diferentes opciones al iniciar sesión.

## Flujo de eventos
1. **Pantalla de login:**
- El actor accede a la interfaz de inicio de sesión.
     
2.**Ingreso de credenciales:**
- El sistema solicita usuario y contraseña.
     
3.**Envío de datos:**
- El actor ingresa los datos y confirma.
     
4.**Validación:**
- El sistema verifica si las credenciales son correctas.
     
5.**Acceso al sistema:**
- Si son válidas, el usuario es redirigido a su panel de control.
      
6.**Manejo de errores:**
- Si no son válidas, el sistema informa el error y permite reintentar.

  ## Condiciones
      
- **Precondiciones:** El usuario debe estar registrado.  
- **Postcondiciones:** El usuario accede a las funcionalidades correspondientes a su rol.

* [Enlace del Escenario](https://drive.google.com/file/d/1YB_A1MMB7P6F8nAOrbXsp2SbcDevWBd5/view?usp=sharing)
 
  ## Caso de uso 3 - Solicitar un turno medico

  ### Descripcion general
  Permite a los pacientes seleccionar especialidad, médico, fecha y hora para generar un nuevo turno. Se verifica la disponibilidad y se notifica al paciente sobre la reserva.

  ## Flujo de eventos
1. **Ingreso al sistema:**
- El paciente inicia sesión con su cuenta.
2. **Acceso a turnos:**
- Selecciona la opción de solicitar un nuevo turno.
3. **Selección de especialidad:**
- Elige entre las especialidades médicas disponibles.
4. **Elección del profesional:**
- El sistema muestra los médicos que atienden esa especialidad.
5. **Consulta de agenda:**
- Se visualiza la disponibilidad del médico seleccionado.
6. **Reserva del turno:**
- El paciente elige día, hora, ingresa el motivo y continúa.
7. **Verificación de disponibilidad:**
- El sistema comprueba si ese turno está libre.
8. **Registro del turno:**
- Si está disponible, se guarda con estado "Pendiente".
9. **Notificación:**
- El paciente recibe confirmación por correo o mensaje.

  ## Condiciones
  
- **Precondiciones:** El paciente debe estar registrado e iniciar sesión.  
- **Postcondiciones:** El turno queda agendado correctamente.

* [Enlace del Escenario](https://drive.google.com/file/d/1aLvmz3u7pHAerV0IJpwEHQgEcwBeYRja/view?usp=sharing)

  ## Caso de uso 4 - Cancelar un turno

  ### Descripcion general
  Este caso de uso permite anular un turno previamente solicitado, liberando el horario en la agenda médica, quedando guardado en el historial de turnos

  ## Flujo de eventos
1. **Acceso a turnos:**
- El actor entra a la sección “Mis turnos”.
2. **Selección del turno:**
- Escoge el turno que desea cancelar.
3. **Confirmación de acción:**
- El sistema solicita que confirme la cancelación.
4. **Ejecución:**
- El actor confirma y el sistema procede con la cancelación.
5. **Cambio de estado:**
- El turno pasa a estado “Cancelado”.
6. **Aviso a involucrados:**
- Se notifica por correo al paciente y al médico.

  ## Condiciones
  
- **Precondiciones:** El turno debe estar en estado pendiente o confirmado.  
- **Postcondiciones:** El turno queda cancelado y libre para otros pacientes.

* [Enlace del Escenario](https://drive.google.com/file/d/1MU8uFkYKamb6EtO7NMyuC-5w-WqrogrK/view?usp=sharing)




