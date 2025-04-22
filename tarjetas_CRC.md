## Tarjetas CRC 


- Las tarjetas CRC (Clase-Responsabilidad-Colaboración) son una herramienta clave en la programación orientada a 
  objetos. Sirven para reconocer y describir las clases 
  más importantes de un sistema, especificando qué funciones deben cumplir y con qué otras clases deben interactuar. 



  ## Tarjeta CRC: Pacinete
- **Clase:** Paciente
    
- **Superclase:** Persona
   
- **Subclases:** –
  
- **Pensamiento del objeto:** “Se que especialista necesito al igual que mis datos personales. Necesito ver con quien y cuando tengo turno medico, avisare cuando no pueda asistir y cancelare mi turno, mis datos pueden cambiar.”
  
- **Responsabilidades:**  
  - Registrarse en el sistema  
  - Solicitar y cancelar turnos  
  - Consultar estado de turnos  
  - Mantener actualizada su información personal
      
- **Colaboradores:** Sistema, Turno, Médico
    
- **Propiedades:**  
  - `nombreCompleto: String`  
  - `dni: String`  
  - `fechaNacimiento: LocalDate`  
  - `telefono: String`  
  - `correo: String`  
  - `historialTurnos: List<Turno>`


![image](https://github.com/user-attachments/assets/e92966b3-96a4-4d9a-8905-a4045a3a4e6e)

[Ver tarjeta CRC](https://drive.google.com/file/d/1VNF_GUc7zUaRyt_1qLDnyki7kYATPH2c/view?usp=sharing)

## Tarjeta CRC: Medico

- **Clase:** Médico
  
- **Superclase:** Persona
  
- **Subclases:** –  
- **Pensamiento del objeto:** “Debo atender pacientes según mi especialidad y disponibilidad, quiero recordar turnos. Necesito ver mi agenda de turnos, quiero registrar diagnosticos y observaciones de mis pacientes. Modificar o cancelar turnos, acceder la historial clinico de mis pacientes”
  
- **Responsabilidades:**  
  - Definir y actualizar su horario de atención  
  - Ver sus turnos programados  
  - Ingresar observaciones médicas
  - Modificar o cancelar turnos
  - Acceder al historial de los pacientes
  
- **Colaboradores:** Turno, Sistema, Paciente, HistoriaClinica, agenda

- **Propiedades:**  
  - `nombreCompleto: String`  
  - `matricula: String`  
  - `especialidad: String`  
  - `horarioAtencion: List<DiaHora>`  
  - `telefono: String`  
  - `correo: String`

  ![image](https://github.com/user-attachments/assets/3bff8d2f-77c6-445a-9d94-bdae90130554)

  [Ver tarjeta CRC](https://drive.google.com/file/d/1hF25AZ768MKmJ5c6Nj_kjFAo1Nzl_J5a/view?usp=sharing)

  ## Tarjeta CRC: Turno

  - **Clase:** Turno
    
- **Superclase:** –
   
- **Subclases:** –
  
- **Pensamiento del objeto:** “Soy un compromiso entre paciente y médico, con fecha y estado definido.”
   
- **Responsabilidades:**  
  - Registrar la solicitud de atención
  - Conocer su fecha y hora  
  - Asociarse a paciente y médico  
  - Almacenar motivo y observaciones  
  - Cambiar su estado
    
- **Colaboradores:** Paciente, Médico, EstadoTurno
  
- **Propiedades:**  
  - `fecha: LocalDate`  
  - `hora: LocalTime`  
  - `estado: EstadoTurno`  
  - `motivo: String`  
  - `observaciones: String`  
  - `paciente: Paciente`  
  - `medico: Médico`

![image](https://github.com/user-attachments/assets/cc1a8dee-7e8a-44b2-a96e-775c9ef76300)


 [Ver tarjeta CRC](https://drive.google.com/file/d/1XXxw1nyf7YSNcVxRgvWFiXlz8_qpZsCo/view?usp=sharing)

 ## Tarjeta CRC: Sistema
 - **Clase:** Sistema
    
- **Superclase:** –
   
- **Subclases:** –
   
- **Pensamiento del objeto:** “Controlo el acceso, organización y gestión de todos los elementos del sistema de turnos.”
    
- **Responsabilidades:** 
  - Validar usuarios y credenciales  
  - Gestionar turnos  
  - Notificar cambios o recordatorios  
  - Manejar reportes y estadísticas
     
- **Colaboradores:** Paciente, Médico, Turno, Notificación
    
- **Propiedades:**  
  - `usuarios: List<Usuario>`  
  - `turnos: List<Turno>`


    [Ver tarjeta CRC]()

    ## Tarjeta CRC: EstadoTurno
    - **Clase:** EstadoTurno
        
- **Superclase:** –
    
- **Subclases:** –
  
- **Pensamiento del objeto:** “Indico en qué etapa del proceso se encuentra un turno.”
   
- **Responsabilidades:**  
  - Representar el estado actual del turno  
  - Validar las transiciones de estado
      
- **Colaboradores:** Turno, Sistema
    
- **Propiedades:**  
  - `estado: Enum (PENDIENTE, CONFIRMADO, CANCELADO, ATENDIDO)`  
  - `fechaCambio: LocalDateTime`

    ## Tarjeta CRC: Notificacion
    - **Clase:** Notificación
       
- **Superclase:** –
  
- **Subclases:** EmailNotificación, SMSNotificación
   
- **Pensamiento del objeto:** “Me encargo de informar al usuario sobre eventos importantes.”
    
- **Responsabilidades:**  
  - Enviar mensajes al paciente o médico  
  - Registrar historial de envíos
      
- **Colaboradores:** Sistema, Paciente / Médico
    
- **Propiedades:**  
  - `tipo: Enum (EMAIL, SMS)`  
  - `contenido: String`  
  - `destinatario: Usuario`  
  - `fechaEnvio: LocalDateTime`



     [Ver tarjeta CRC]()





