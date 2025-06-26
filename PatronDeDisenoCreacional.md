Anexo - Aplicación de Patrón de Diseño Creacional - Factory Method

¿Qué son los patrones de diseño creacionales?

Los patrones de diseño creacionales abordan el problema de la creación de objetos, separando la lógica de instancia del resto del sistema. Ayudan a cumplir el principio SOLID de responsabilidad única (SRP), permitiendo que las clases no sean responsables de su propia creación, y favoreciendo la extensibilidad (OCP).

📅 Propósito y Tipo del Patrón

El patrón Factory Method se utiliza para delegar la instanciación de objetos a una jerarquía de clases, permitiendo crear diferentes tipos de turnos sin modificar la lógica principal del sistema.

💡 Motivación

En el sistema de gestión de turnos médicos, la clase ServicioTurno era responsable de crear objetos Turno de manera directa. Esto generaba un acoplamiento innecesario y dificultaba la incorporación de nuevas variantes de turno (por ejemplo, turnos presenciales, virtuales, urgentes).

Aplicando el patrón Factory Method, introducimos una interfaz TurnoFactory con un método crearTurno(...), y clases concretas como TurnoPresencialFactory, TurnoVirtualFactory, etc. Esto permite delegar la creación del objeto Turno, facilitando la extensión del sistema sin modificar código existente.
