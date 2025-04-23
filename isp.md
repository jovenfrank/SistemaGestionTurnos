# Principio de Segregacion de Interfaces (ISP)

En el sistema de gestión de turnos médicos, uno de los problemas identificados fue que ciertos módulos del sistema estaban obligados a depender de funcionalidades que no utilizaban. Por ejemplo, un componente que simplemente se encargaba de mostrar turnos también debía incluir funciones relacionadas con informes estadísticos, configuración del sistema o administración de usuarios. Este inconveniente se debe a una violación del principio de segregación de interfaces (ISP), que establece que ningún módulo debe estar obligado a depender de métodos que no necesita. Es decir, cada parte del sistema debe contar solamente con lo esencial para funcionar.

El principio ISP (Interface Segregation Principle) propone dividir esas interfaces grandes en partes más pequeñas y específicas, de modo que cada componente del sistema dependa únicamente de lo que realmente requiere. Al aplicar este principio, se desarrollaron interfaces más simples y enfocadas, como una para la gestión de turnos, otra para notificaciones y una más para reportes.

## Motivacion

En el sistema de gestión de citas médicas, uno de los problemas identificados fue que ciertos módulos del sistema estaban obligados a depender de funcionalidades que no utilizaban. Por ejemplo, un componente que simplemente se encargaba de mostrar turnos también debía incluir funciones relacionadas con informes estadísticos, configuración del sistema o administración de usuarios. Este inconveniente se debe a una violación del principio de segregación de interfaces (ISP), que establece que ningún módulo debe estar obligado a depender de métodos que no necesita. Es decir, cada parte del sistema debe contar solamente con lo esencial para funcionar.

Para aplicar este principio, se fragmentaron las grandes estructuras en interfaces más pequeñas y especializadas, enfocadas en tareas específicas. Así, por ejemplo, el módulo de visualización de turnos depende únicamente de una interfaz que contiene funciones de visualización; el módulo de informes depende de una interfaz que exclusivamente maneja reportes, y así sucesivamente. Esto hace que cada parte del sistema sea más simple, más estable y más fácil de mantener o modificar sin riesgos innecesarios.

**Ejemplo del mundo real**

Imagina un restaurante donde el mesero tiene que usar una tableta para tomar órdenes, pero también está obligado a acceder a funciones de gestión de inventario y control de empleados que no necesita en ese momento. Esto hace que el mesero se distraiga y le cueste mucho más tiempo tomar la orden del cliente. Si en cambio, cada mesero tuviera una aplicación diseñada exclusivamente para tomar órdenes y gestionar mesas, podría concentrarse en lo que realmente es importante y ofrecer un mejor servicio al cliente. De esta manera, cada parte del sistema se adapta a las necesidades específicas de sus usuarios.

## Estructura de Clases

![image](https://github.com/user-attachments/assets/4e2f1dba-f7cc-42d3-940b-489807887d58)

[Visualizar en Drive](https://drive.google.com/file/d/1NlxmEdCLyOSBsplyrHnyzZBI50YRTKuo/view?usp=sharing)



