# Herramientas agile.

## Tarjetas CRC

Las Tarjetas CRC (Clase, Responsabilidad, Colaborador) se utilizaron para modelar las clases principales del sistema de gestión de turnos médicos, detallando sus responsabilidades, colaboraciones, pensamiento del objeto y propiedades.

### Tarjeta CRC: Paciente

**Nombre de la Clase:** Paciente
**Superclase:**
**Subclase:**
**Pensamiento del objeto:** Sé qué especialidad necesito y mis datos personales. Quiero ver cuándo y con quién tengo turno. Necesito avisar que no podré asistir. Mis datos pueden cambiar. Quiero recordar mis visitas anteriores.
**Responsabilidades:** Solicitar un turno, Consultar sus turnos programados, Cancelar un turno, Actualizar sus datos personales, Ver el historial de sus consultas.
**Colaboradores:** Agenda, Turno, Médico.
**Propiedad:** nombre, apellido, fechaNacimiento, DNI, nroHistoriaClinica.



   **Superclase:** Sistema 

   **Subclase:** -


- Pensamiento del objeto: El usuario debe conocer los datos del turno que va a cancelar y notificar la cancelacion 
  del turno.

- Responsabilidades: El usuario debe poder cancelar el turno y notificar la cancelacion.

- Colaboradores: Solicitud de Turno, Notificacion.

- Propiedad: Usuario, dia fecha y hora del turno, especialidad, medico. 


![Captura de pantalla 2025-04-13 195554](https://github.com/user-attachments/assets/60fbc1a3-dea8-475e-b8e4-e593647c5ca9)
