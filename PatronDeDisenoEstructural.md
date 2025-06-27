# Anexo - Aplicación de Patrón de Diseño Estructural - Adapter

## ¿Qué son los Patrones de Diseño Estructurales?

Los patrones estructurales se centran en **cómo componer clases y objetos** para formar estructuras más grandes y flexibles, facilitando la reutilización y el mantenimiento. Se encargan de adaptar, encapsular o unir componentes del sistema sin modificar sus interfaces internas.

Estos patrones están estrechamente relacionados con los principios SOLID, especialmente con:
- **OCP (Open/Closed Principle)**: Abierto a extensión pero cerrado a modificación.
- **DIP (Dependency Inversion Principle)**: El código de alto nivel no debe depender del de bajo nivel directamente.

## Propósito y Tipo del Patrón

**Patrón utilizado**: Adapter  
**Propósito**: Adaptar distintas formas de notificación externa (email, SMS, WhatsApp) sin modificar la lógica del sistema, encapsulando los detalles de cada proveedor bajo una misma interfaz.  
**Tipo**: Patrón de diseño estructural.

## Motivación

En nuestro sistema de gestión de turnos, la clase `Notificador` era responsable de enviar mensajes al paciente o al médico al registrar, cancelar o confirmar turnos. Sin embargo, si en el futuro el sistema necesita enviar notificaciones a través de distintos canales (por ejemplo, SMS, Email o WhatsApp), modificar la clase `Notificador` directamente cada vez violaría el principio de **abierto/cerrado**.

Para resolver este problema, utilizamos el patrón Adapter. Creamos una **interfaz común llamada `INotificador`**, que define el método `enviar(mensaje: string): void`, y diferentes adaptadores (`EmailAdapter`, `SMSAdapter`, `WhatsAppAdapter`) que encapsulan la lógica específica para cada canal. Así, cualquier clase del sistema puede usar una instancia de `INotificador` sin preocuparse por la implementación concreta.

## Clases implicadas
![DiagramaClase](https://github.com/abartomioli/SistemaGestionTurnos/blob/main/ImgPOO/Adapter.jpg)
