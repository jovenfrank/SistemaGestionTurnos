# Principio de Sustitucion de Liskov (LSP)

Este principio se refiere a la herencia y sustitución de objetos en la programación orientada a objetos. Su objetivo es asegurar que las subclases puedan reemplazar a sus clases base sin modificar el comportamiento esperado del sistema. En un sistema de gestión de citas médicas, se desarrolló una clase principal llamada Usuario y varias subclases, como Paciente, Médico y Administrador. Sin embargo, algunas de estas subclases sobrescribían métodos heredados de manera que alteraban la lógica general del sistema. Por ejemplo, si un método esperaba un objeto de tipo Usuario y se le proporcionaba un Administrador, podría fallar, ya que este último no implementaba correctamente un comportamiento esperado, como la programación de citas.

## Motivacion

Uno de los desafíos más significativos que enfrentaba el sistema de gestión de citas médicas era la manera en que se habían clasificado y organizado los diferentes tipos de usuarios del sistema. Existía una categoría amplia para todos los usuarios, de la cual se derivaban otros perfiles, como pacientes, médicos y administradores. El inconveniente surgía cuando se asumía que todos estos usuarios podían realizar las mismas acciones, lo cual no era correcto. Por ejemplo, el sistema intentaba permitir que cualquier usuario pudiera solicitar citas médicas, cuando en realidad solo los pacientes deberían tener esa facultad.

Esta suposición equivocada provocaba que el sistema se volviera inconsistente. Era necesario realizar excepciones dentro del mismo funcionamiento para que los administradores, por ejemplo, no pudieran solicitar citas, a pesar de estar dentro del grupo general de “usuarios”. Esto complicaba el mantenimiento, introducía errores y hacía que el sistema fuera menos confiable a lo largo del tiempo.

Aquí es donde entra el principio de sustitución de Liskov, uno de los principios SOLID. Este principio establece que si algo pertenece a un grupo, debe comportarse como se espera dentro de ese grupo, sin causar problemas. Es decir, si alguien es considerado un usuario, entonces debería poder llevar a cabo las acciones esperadas para un usuario, sin necesidad de hacer excepciones o ajustes especiales.

Para solucionar el problema, se reorganizó la manera en que se definían los perfiles. En lugar de suponer que todos los usuarios pueden hacer lo mismo, se definieron con claridad qué tipo de acciones puede realizar cada uno. Así, los pacientes pueden solicitar citas, los médicos pueden atenderlas y los administradores pueden gestionar el sistema. De este modo, se evitan errores y se asegura que cada tipo de usuario actúe únicamente dentro de sus responsabilidades.

**Un ejemplo del mundo real**

Imaginemos que en una empresa todos los empleados cuentan con una tarjeta de acceso. Sin embargo, solo los ingenieros pueden ingresar al laboratorio. Si se permite que todos los empleados usen la misma tarjeta para cualquier área, entonces será necesario hacer excepciones cada vez que un empleado sin autorización quiera acceder al laboratorio. En cambio, si desde el principio se asignan accesos específicos según el rol de cada persona, no será necesario estar revisando constantemente quién puede hacer qué. El sistema funcionará de manera más ordenada, segura y clara.

## Estructura de Clases

![image](https://github.com/user-attachments/assets/526ac570-018f-4d5d-99ee-ea543f8e4b1c)

[Visualizar en Drive](https://drive.google.com/file/d/1G6JwNs_y_1Ffkzxr6PPqUYKMsMHW9kme/view?usp=sharing)
