# Principio Abierto/Cerrado (OCP)

El objetivo principal del Principio de Abierto/Cerrado es permitir que el software sea extensible para nuevas funcionalidades sin necesidad de modificar su código ya existente. En el sistema de gestión de turnos médicos, la funcionalidad de notificaciones estaba diseñada de forma rígida. Toda la lógica para enviar correos, mensajes de texto o llamadas estaba dentro de una misma estructura. Cada vez que se necesitaba agregar un nuevo tipo de notificación (como WhatsApp o notificaciones móviles), era necesario modificar directamente el código existente. Esto generaba errores, rompía funcionalidades previas y complicaba el mantenimiento del sistema.

El principio OCP propone que el sistema debe estar abierto para extenderse, pero cerrado para ser modificado. Es decir, debería poder agregarse una nueva funcionalidad (como un nuevo tipo de notificación) sin tocar el código que ya funciona. Para lograrlo, se reorganizó la lógica en componentes independientes, donde cada tipo de notificación tiene su propia estructura. Así, si se quiere añadir otro canal de aviso, se hace como una extensión, sin afectar lo anterior. Esto vuelve al sistema más flexible, seguro y preparado para el cambio.

## Motivacion

En el contexto del sistema de gestión de turnos médicos, uno de los desafíos más comunes surge al intentar añadir nuevas funcionalidades, como la implementación de distintos tipos de notificaciones para pacientes y médicos. Inicialmente, el sistema estaba diseñado para enviar únicamente correos electrónicos, pero pronto se buscaron añadir mensajes de texto, notificaciones móviles y otros canales de comunicación.

El problema principal era que cada vez que se quería incluir un nuevo método de notificación, era necesario alterar la lógica ya establecida. Esto ocasionaba diversos inconvenientes: podían surgir errores en funcionalidades que ya estaban funcionando correctamente, se complicaba la ejecución de pruebas y el sistema se volvía cada vez más frágil y difícil de mantener.

El principio de abierto/cerrado (OCP) presenta una solución efectiva: los sistemas deben ser accesibles para la adición de nuevas funcionalidades, pero deben permanecer cerrados a modificaciones internas. En otras palabras, no se debe modificar lo que ya está operativo; en lugar de eso, hay que incorporar nuevas características como módulos que se integran al sistema existente.

**Ejemplo del mundo real**

Un ejemplo práctico sería una máquina expendedora diseñada inicialmente para ofrecer solo tres opciones de bebidas. Si cada nueva bebida requiere que se reprograme la lógica principal, el mantenimiento del sistema se vuelve complicado. Sin embargo, si cada nueva bebida se gestiona como un módulo independiente, sumarla resulta tan sencillo como conectar una nueva unidad, sin necesidad de alterar las que ya están en funcionamiento.

## Estructura de clases

![image](https://github.com/user-attachments/assets/f6d056e4-b40c-40c1-9bc2-cc4e89eb602e)

[Visualizar en Drive](https://drive.google.com/file/d/1KawgU_eZ44O0f_qrTlcU71Ib_eM4Oe2F/view?usp=sharing)
