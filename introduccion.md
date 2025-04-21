# 📖 Introducción

##  Programación Orientada a Objetos (POO)

La **Programación Orientada a Objetos (POO)** es un paradigma de programación que se basa en la creación y manipulación de "objetos", los cuales representan entidades del mundo real. Es fundamental porque permite:
- Modularidad: División del código en partes reutilizables.
- Reutilización: Uso de clases y herencia para evitar código duplicado.
- Mantenimiento: Facilita la actualización y mejora del código.

---

##  Los Cuatro Fundamentos de POO

### 1️⃣ **Encapsulamiento**
   - Agrupar datos y métodos en una sola unidad (clase).
   - Ejemplo: Un automóvil (clase) tiene atributos como "marca" y "color", y métodos como "acelerar" y "frenar".  
   
### 2️⃣ **Herencia**
   - Permite que una clase (hija) herede atributos y métodos de otra clase (padre).
   - Ejemplo: Un "AutoDeportivo" hereda características de "Automóvil".

### 3️⃣ **Polimorfismo**
   - Un mismo método puede comportarse de manera diferente en distintas clases.
   - Ejemplo: Un "Empleado" puede tener un método "calcularSalario()", pero su implementación varía entre un "Gerente" y un "Vendedor".

### 4️⃣ **Abstracción**
   - Permite crear clases genéricas sin preocuparse por los detalles internos.
   - Ejemplo: Un "DispositivoElectrónico" puede tener métodos como "encender()" y "apagar()", pero su implementación varía para un "Teléfono" y una "Computadora".

---

## 📋 Requisitos Iniciales del Sistema

1. Permitir a los usuarios registrarse y solicitar turnos.
2. Generar y administrar turnos de manera automática.
3. Notificar a los usuarios sobre la asignación de turnos.
4. Permitir la consulta del estado de un turno en tiempo real.
5. Gestionar diferentes tipos de turnos según el servicio requerido.

---

## 📌 Casos de Uso

## ✅ Caso de Uso 1: Registrar Paciente

- **Actor(es)**: Sistema / Paciente  
- **Descripción breve**: Permite registrar a un nuevo paciente en el sistema con toda su información personal.  
- **Flujo principal de eventos**:
  1. El paciente accede al módulo de “Registro de Paciente”.
  2. El sistema solicita los siguientes datos:
     * Nombre completo
     * DNI / Documento
     * Fecha de nacimiento
     * Teléfono
     * Correo electrónico
     * Dirección
  3. El paciente completa y envía el formulario.
  4. El sistema valida los datos (que no exista otro paciente con el mismo DNI o email).
  5. Si todo es correcto, se guarda el nuevo registro.
  6. Se muestra un mensaje de confirmación.
- **Precondiciones**: El paciente no debe estar registrado previamente.  
- **Postcondiciones**: Paciente registrado correctamente en la base de datos.

---

## ✅ Caso de Uso 2: Iniciar Sesión al Sistema

- **Actor(es)**: Administrador / Médico / Paciente  
- **Descripción breve**: El usuario accede al sistema usando sus datos personales
- **Flujo principal de eventos**:
  1. El paciente accede a la pantalla de inicio de sesión.
  2. Ingresa su nombre de usuario o correo electrónico y contraseña.
  3. El sistema valida las credenciales.
  4. Si son válidas, se redirige al panel correspondiente según el rol.
  5. Si no son válidas, se muestra un mensaje de error.
- **Precondiciones**: El usuario debe estar previamente registrado.
- **Postcondiciones**: Acceso concedido al sistema, según el tipo de usuario.

---

## ✅ Caso de Uso 3: Solicitar un Turno Nuevo

- **Actor(es)**: Paciente / Sistema
- **Descripción breve**: El paciente solicita un nuevo turno segun la especialidad que desee, medicos disponibles, fecha y horario.
- **Flujo principal de eventos**:
  1. El paciente accede a la opción “Solicitar Turno”.
  2. Selecciona la especialidad médica deseada.
  3. El sistema muestra los médicos disponibles con esa especialidad.
  4. El paciente selecciona un médico.
  5. El sistema muestra el calendario con los horarios disponibles.
  6. El paciente elige una fecha y hora.
  7. Ingresa el motivo del turno y, opcionalmente, observaciones.
  8. El sistema registra el turno con estado "pendiente" o "confirmado".
  9. Se muestra una confirmación y se envía una notificación al paciente.
- **Precondiciones**: El paciente debe estar registrado.  
- **Postcondiciones**: Turno agendado en la agenda médica correspondiente.

---

## ✅ Caso de Uso 4: Cancelar un Turno

- **Actor(es)**: Paciente / Médico / Sistema 
- **Descripción breve**: Permite cancelar un turno previamente asignado.  
- **Flujo principal de eventos**:
  1. El paciente accede a la sección de “Mis Turnos”.
  2. Selecciona el turno que desea cancelar.
  3. Confirma la acción.
  4. El sistema cambia el estado del turno a "cancelado".
  5. Se envía una notificación a los involucrados (paciente y médico).
- **Precondiciones**: Debe haber un turno previamente asignado al paciente  
- **Postcondiciones**: El turno queda cancelado y reflejado en el historial.

---

## ✅ Caso de Uso 5: Ver Estado del Turno

- **Actor(es)**: Paciente / Sistema 
- **Descripción breve**: Permite visualizar el estado de los turnos del paciente.  
- **Flujo principal de eventos**:
  1. El paciente accede a la opción “Mis Turnos”.
  2. El sistema muestra una lista de turnos con su información:
     - Fecha y hora
     - Médico asignado
     - Estado del turno (pendiente, confirmado, cancelado)
     - Motivo y observaciones
  3. El usuario puede filtrar por estado o fecha.
- **Precondiciones**: El paciente debe estar registrado y tener turnos asociados.  
- **Postcondiciones**: El usuario obtiene una vista clara del estado de sus turnos.

  # Boceto Inicial del Diseño de Clases
  ![Untitled-2025-04-14-1414](https://github.com/user-attachments/assets/506c67c8-4c9c-4f0b-a393-e176b7b7f2d4)
  
  [Enlace para visualizar el boceto en linea](https://drive.google.com/file/d/1ZcqSf7J5FQL3zummXjd3QpSjbuT-l5sZ/view?usp=drive_link)


