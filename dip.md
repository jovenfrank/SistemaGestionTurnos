# Principio de Inversion de Dependencias (DIP)

En el sistema de gestión de turno médicos, algunos módulos clave estaban conectados directamente a servicios específicos, como una base de datos determinada o un sistema particular de envío de correos electrónicos. Esto significaba que cualquier modificación en esos servicios impactaba directamente en todo el sistema, generando errores y complicando la evolución o migración hacia nuevas tecnologías.

Este principio sugiere invertir las dependencias: en lugar de que la lógica central del sistema dependa directamente de servicios concretos, se trabaja con abstracciones (por ejemplo, utilizando un "servicio de notificación" en lugar de un "servicio de correo"). Así, se pueden cambiar o sustituir los servicios reales sin alterar el funcionamiento principal del sistema. Esto permite que el sistema sea mucho más flexible, reutilizable y fácil de adaptar con el tiempo.

## Motivacion

En el sistema de gestión de turno medicos, uno de los mayores problemas era que los módulos de alto nivel (como la lógica principal del sistema, que gestiona la programación de citas y la asignación de médicos) dependían directamente de implementaciones de bajo nivel (como bases de datos específicas o sistemas de notificación, como el correo electrónico). Este enfoque hacía que cualquier cambio en estos componentes de bajo nivel tuviera un gran impacto en toda la aplicación.

Al aplicar el Principio de Inversión de Dependencias (DIP), el sistema fue reestructurado para que la lógica principal del sistema dependiera de abstracciones (como interfaces de notificación, bases de datos y servicios) en lugar de implementaciones concretas. Por ejemplo, en lugar de que el sistema de gestión de citas dependa directamente de un servicio de correo electrónico específico, se creó una interfaz general de "Servicio de Notificación", y el sistema interactúa con esta interfaz, sin saber qué servicio de notificación está siendo utilizado realmente. Esto permitió cambiar o reemplazar el sistema de notificación sin afectar el resto del sistema. El código de alto nivel se desacopló de los detalles de implementación, haciendo que el sistema fuera más flexible, fácil de probar y más sencillo de mantener a largo plazo.

**Ejemplo del mundo real**

Imaginemos que una empresa de videojuegos tiene una aplicación que gestiona la compra y descarga de juegos. Originalmente, la aplicación está diseñada para interactuar directamente con un sistema de pago específico. Si la empresa decide cambiar a otro proveedor de pagos, tendría que modificar toda la aplicación para adaptarse a las nuevas herramientas del nuevo proveedor, lo cual puede ser complicado y propenso a errores.

Sin embargo, si la aplicación está construida para depender de una interfaz común de "Sistema de Pago" (en lugar de depender directamente de un proveedor específico), solo necesitaría cambiar la implementación de esa interfaz para reflejar el nuevo proveedor de pagos. Esto permite una gran flexibilidad y agilidad ante cambios en el futuro, además de reducir los riesgos de errores, ya que solo se modifica una pequeña parte del sistema.

![image](https://github.com/user-attachments/assets/26b9edad-cc65-4b14-9923-ff1c338fb256)

[Visualizar en Drive](https://drive.google.com/file/d/197GojyAh9SFTRdAzJfM0djmWiuyi2w6c/view?usp=sharing)


