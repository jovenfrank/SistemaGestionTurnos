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
  1. El usuario ingresa sus datos.  
  2. El sistema valida la información.  
  3. Se confirma el registro.  
- **Precondiciones:** Ninguna.  
- **Postcondiciones:** El usuario queda registrado en el sistema.  

###  **Caso de Uso 2: Solicitar Turno**
- **Actor:** Usuario  
- **Descripción:** Permite a los usuarios solicitar un turno.  
- **Flujo Principal:**  
  1. El usuario selecciona un servicio.  
  2. El sistema genera un turno.  
  3. Se asigna un número de turno al usuario.  
- **Precondiciones:** El usuario debe estar registrado.  
- **Postcondiciones:** Se genera y asigna un turno.  

###  **Caso de Uso 3: Consultar Estado del Turno**
- **Actor:** Usuario  
- **Descripción:** Permite a los usuarios ver el estado de su turno en tiempo real.  
- **Flujo Principal:**  
  1. El usuario ingresa su número de turno.  
  2. El sistema muestra el estado del turno.  
- **Precondiciones:** El usuario debe tener un turno generado.  
- **Postcondiciones:** Se muestra la información del turno.  

###  **Caso de Uso 4: Cancelar Turno**
- **Actor:** Usuario  
- **Descripción:** Permite a los usuarios cancelar un turno asignado.  
- **Flujo Principal:**  
  1. El usuario selecciona un turno activo.  
  2. Confirma la cancelación.  
  3. El sistema elimina el turno.  
- **Precondiciones:** El usuario debe tener un turno activo.  
- **Postcondiciones:** El turno se elimina del sistema.  

###  **Caso de Uso 5: Generar Reportes de Turnos**
- **Actor:** Administrador  
- **Descripción:** Permite al administrador generar reportes sobre turnos atendidos.  
- **Flujo Principal:**  
  1. El administrador selecciona un rango de fechas.  
  2. El sistema muestra los reportes generados.  
- **Precondiciones:** El administrador debe tener permisos.  
- **Postcondiciones:** Se genera un reporte de turnos.
  # Boceto de Turnos
  Para ver el boceto sobre la gestion de turnos haga click [Aqui](boceto.md)
