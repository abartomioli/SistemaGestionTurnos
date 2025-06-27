# Anexo - Aplicación de Patrón de Diseño de Comportamiento - Observer

## ¿Qué son los patrones de comportamiento y para que se utiliza?
Los patrones de diseño de comportamiento se enfocan en cómo los objetos interactúan y se comunican entre sí. Estos patrones ayudan a reducir el acoplamiento entre objetos y promueven un sistema más flexible y mantenible. Se relacionan con los principios SOLID, especialmente con el Principio de Inversión de Dependencias (DIP) y el Principio de Responsabilidad Única (SRP), ya que separan las responsabilidades de notificación del resto del sistema.

El patrón Observer se utiliza cuando un objeto necesita notificar a varios otros objetos sobre cambios en su estado, sin estar directamente acoplado a ellos. Es ideal cuando múltiples componentes deben reaccionar ante un evento en común, como en nuestro caso, el cambio de estado de un turno.

## Motivación
En el sistema de gestión de turnos, cuando un turno cambia de estado (por ejemplo, se confirma, cancela o reprograma), deben realizarse varias acciones:
El Paciente debe recibir una notificación.
El Médico debe ser informado del cambio.
El Notificador puede encargarse de enviar correos o mensajes.

En el diseño original, esto estaba acoplado dentro de la clase Turno, generando alta dependencia y poca flexibilidad. Con el patrón Observer, ahora Turno se convierte en el Subject que mantiene una lista de observadores, y cada uno de ellos puede reaccionar al evento de forma desacoplada, simplemente implementando una interfaz IObservador.

## Clases implicadas
![DiagramaClase](https://github.com/abartomioli/SistemaGestionTurnos/blob/main/ImgPOO/Observer.jpg?raw=true)
![DiagramaClase](https://github.com/abartomioli/SistemaGestionTurnos/blob/main/ImgPOO/Observer.jpg)
