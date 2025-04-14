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

###  **Caso de Uso 1: Registro de Usuario**
- **Actor:** Usuario
   
- **Descripción:** Permite a los usuarios registrarse en el sistema.
  
- **Flujo Principal:**  
  1. El usuario ingresa al sistema para registrarse.  
  2. El sistema muestra un formulario en el cual pide datos del paciente (Nombre y apellido completo, DNI, numero telefonico, Correo electronico.  
  3. El usuario ingresa todos los datos necesarios.
  4. El sistema valida los datos ingresados (Para validar el correo y numero telefonico envia un codigo).
  5. Los datos son registrados y guardados en el sistema.
  6. El sistema muestra un mensaje de "Registrado con exito"  
- **Precondiciones:** Ninguna.
    
- **Postcondiciones:** El usuario queda registrado en el sistema.  

###  **Caso de Uso 2: Solicitar Turno**

- **Actor:** Usuario
  
- **Descripción:** Permite a los usuarios solicitar un turno.
  
- **Flujo Principal:**  
  1. El usuario ingresa con su cuenta previamente creada.
  2. El sistema verifica si los datos son correctos  
  3. El usuario selecciona el apartado de solicitar un turno.  
  4. El sistema muestra los turnos disponibles acorde a una fecha, horario, especialidad y un medico.
  5. El ususario selecciona la especialidad, fecha, horario y medico.
  6. El sistema verifica si esta disponible dicha fecha y medico.
  7. En caso de estar disponible el sistema muestra un mensaje de "Turno Asignado" y le genera un codigo de seguimiento sobre el turno, en caso de no estar disponible el sistema pedira que seleccione un horario o fecha diferente.

- **Precondiciones:** El usuario debe estar registrado.
    
- **Postcondiciones:** Se genera y asigna un turno.  

###  **Caso de Uso 3: Consultar Estado del Turno**

- **Actor:** Usuario
  
- **Descripción:** Permite a los usuarios ver el estado de su turno en tiempo real.
   
- **Flujo Principal:**  
  1. El usuario ingresa con su cuenta al sistema.  
  2. El sistema verifica si los datos son correctos.
  3. El usuario selecciona el apartado de Turnos - Estado de turno.
  4. El sistema pide el codigo de seguimiento del turno.
  5. El usuario ingresa el codigo de seguimiento previamente dado al solicitar el turno.
  6. El sistema verifica el codigo.
  7. El sitema muestra el estado del turno del usuario.  
- **Precondiciones:** El usuario debe tener un turno generado.
   
- **Postcondiciones:** Se muestra la información del turno.  

###  **Caso de Uso 4: Cancelar Turno**

- **Actor:** Usuario
  
- **Descripción:** Permite a los usuarios cancelar un turno asignado.
   
- **Flujo Principal:**  
  1. El usuario ingresa al sistema con sus datos.
  2. El sistema verifica la informacion.  
  3. El usuario ingresa al apartado de Turnos - Cancelar turno.
  4. El sistema pide el codigo del turno.
  5. El usuario ingresa el codigo de seguimiento.
  6. El sistema verifica el codigo y da acceso al apartado de cancelar turno.
  7. El usuario da click en el apartado de Cancelar turno
  8. El sistema imprime un mensaje de "Seguro que quieres cancelar el turno" y da dos opciones "Si" o "No"
  9. El usuario seleccion en el apartado de "Si"
  10. El sistema muestra un mensaje de "Turno cancelado"
  11. El sistema elimina el turno.  
- **Precondiciones:** El usuario debe tener un turno activo.
   
- **Postcondiciones:** El turno se elimina del sistema.  

###  **Caso de Uso 5: Notificación de turno próximo

- **Actor:**  Usuario, Sistema de Gestión de Turnos
  
- **Descripción:**  
  El sistema envía una notificación automática al usuario cuando su turno se aproxima, para recordarle la fecha y hora asignada.
  
- **Flujo principal:**
  1. El usuario solicita un turno a través del sistema.
  2. El sistema registra la información del turno con fecha y hora.
  3. Cuando el turno se encuentra a menos de 24 horas, el sistema detecta automáticamente la proximidad del evento.
  4. El sistema genera una notificación personalizada.
  5. El sistema envía la notificación al usuario por correo electrónico o mensaje dentro de la plataforma.
  6. El usuario recibe la notificación y se prepara para asistir a su turno.
     
- **Precondiciones:**
  - El usuario debe haber agendado un turno en el sistema.
  - El usuario debe tener una dirección de correo válida registrada.
    
- **Postcondiciones:**
  - El usuario recibe una notificación con la información de su turno.
  - El evento queda registrado en el historial del sistema. 

  # Boceto Inicial del Diseño de Clases
  Para ver el boceto sobre la gestion de turnos haga click [Aqui](boceto.md)
