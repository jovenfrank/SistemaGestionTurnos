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
   
- **Pensamiento del objeto:** “Soy el núcleo del sistema de gestión de turnos y almaceno todos los datos. Coordino las acciones principales, gestiono la interacción entre usuarios, médicos, pacientes y turnos. Me encargo de mantener la integridad de los datos y brindar acceso a las funcionalidades clave del sistema. Debo registrar a usuarios nuevos al igual que profesionales. Valido las credenciales de cada usuario que ingresa al sistema. Necesito enviar notificaciones en tiempo y forma”
    
- **Responsabilidades:**

Registrar nuevos usuarios y médicos en el sistema 
Validar credenciales e iniciar sesión  
Gestionar solicitudes de turnos  
Verificar disponibilidad de turnos para médicos  
Coordinar el envío de notificaciones a los pacientes  
Guardar cambios en la base de datos o almacenamiento persistente  
Controlar accesos y roles (administrador, paciente, médico)
     
- **Colaboradores:** Paciente, Médico, Turno, Notificación, administrador


- **Propiedades:**
- `listaPacientes: List<Paciente>`  
- `listaMedicos: List<Medico>`  
- `listaTurnos: List<Turno>`  
- `usuariosRegistrados: List<Usuario>`  
- `notificador: Notificador`  
- `sistemaActivo: boolean`  
- `registroEventos: List<String>` (para log de actividades)

![image](https://github.com/user-attachments/assets/9fb32266-7db6-4abd-bc0f-aff02e3f9cf3)

[Ver tarjeta CRC](https://drive.google.com/file/d/1AFv_JSxsycmW9GPjU6Rtr_vlg07U4xjI/view?usp=sharing)

    
## Tarjeta CRC: EstadoTurno
- **Clase:** EstadoTurno
        
- **Superclase:** –
    
- **Subclases:** –
  
- **Pensamiento del objeto:** “Represento el estado actual de un turno dentro del sistema. Debo dar descripciones precisas y correctas de los turnos. Indico si un turno está confirmado, cancelado, pendiente o finalizado. Soy esencial para el seguimiento, gestión y validación del flujo de turnos, Conozco las reglas de comportamiento, si un turno esta asignado no se mostrara como disponible”
   
- **Responsabilidades:**  
- Almacenar y exponer el estado actual de un turno  
- Validar transiciones entre estados válidos (por ejemplo, de 'pendiente' a 'confirmado')  
- Proveer descripciones comprensibles del estado para mostrar al usuario  
- Notificar al sistema sobre cambios en el estado del turno  
- Asociar reglas de comportamiento según el estado (por ejemplo, si un turno está asignado, no debe mostrarse como disponible)
      
- **Colaboradores:** Turno, Sistema, Notificador
    
- **Propiedades:**  
- `estadoActual: String` (valores posibles: `"pendiente"`, `"confirmado"`, `"cancelado"`, `"finalizado"`)  
- `fechaCambio: LocalDateTime` (marca temporal del último cambio de estado)  
- `descripcion: String` (explicación opcional del motivo del cambio de estado)  
- `turnoAsociado: Turno` (referencia al turno al que pertenece este estado)

**Posibles extensiones:**

- Agregar historial de cambios de estado  
- Asociar códigos de notificación para cambios automáticos  
- Incluir un campo `usuarioQueCambio` para rastrear quién cambió el estado

![image](https://github.com/user-attachments/assets/3355928e-ab02-4cf3-9c10-800c509b36a4)

[Ver tarjeta CRC](https://drive.google.com/file/d/18h8KJ25oqO1vTykdLxQavAwK_lrXaP2i/view?usp=sharing)





