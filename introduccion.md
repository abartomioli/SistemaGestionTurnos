#Introducción

## Anexo - Introducción al Diseño Orientado a Objetos

### ¿Qué es el paradigma de programación orientada a objetos (POO)?
La Programación Orientada a Objetos (POO) es un paradigma de programación basado en la organización del código en objetos, los cuales representan entidades del mundo real y encapsulan datos (atributos) y comportamientos (métodos).

Este enfoque permite estructurar el código de manera modular y reutilizable, favoreciendo el mantenimiento y la escalabilidad de los programas.

### Principales conceptos de la POO
- Clases: Son moldes o plantillas que definen las características y comportamientos de los objetos.
- Objetos: Son instancias de una clase y contienen datos específicos.
- Encapsulamiento: Restricción del acceso a los datos internos de un objeto para proteger la integridad de la información.
- Herencia: Permite que una clase derive de otra, reutilizando código y fomentando la jerarquía de clases.
- Polimorfismo: Capacidad de los objetos de responder de manera diferente a un mismo mensaje o método.
- Abstracción: Simplificación de la realidad mediante la definición de solo las características esenciales de un objeto.

### Por qué es importante la POO?
- Reutilización de código: Permite evitar la duplicación de código mediante la herencia y la modularidad.
- Mantenimiento y escalabilidad: Facilita la modificación y expansión del sistema sin afectar otras partes del código.
- Modularidad: Separa la lógica en componentes independientes y reutilizables.
- Seguridad y robustez: El encapsulamiento protege los datos y reduce errores en la manipulación de información.
- Facilidad para modelar el mundo real: Representa problemas complejos de manera más intuitiva y organizada.


## Anexo - Los cuatro fundamentos de POO
### Los cuatros fundamentos de POO son:
  1 - Encapsulamiento
  2 - Herencia
  3 - Polimorfismo
  4 - Abstracción

#### 1) Encapsulamiento:
Es el principio que protege los datos de un objeto restringiendo su acceso desde fuera de la clase. Solo se puede interactuar con los datos a través de métodos específicos.

##### - Ejemplo: Un cajero Automático
  - Los datos de la cuenta (saldo, número de cuenta) están protegidos.
  - El usuario solo puede interactuar a través de métodos como "Retirar dinero" o "Consultar saldo".

***-------CAJERO ATM-------***<br>
-------INGRESAR PIN------<br>
---CONSULATAR SALDO--<br>
-----RETIRAR DINERO-----<br>

#### 2) Herencia
Permite que una clase (subclase) herede atributos y métodos de otra clase (superclase), reutilizando código y estableciendo jerarquías.

##### - Ejemplo: Vehículos
  - Una clase genérica "Vehículo" tiene atributos como "color", "número de ruedas", "velocidad".
  - Las subclases "Auto" y "Moto" heredan estos atributos y pueden agregar características propias.

 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Vehículo<br>
  ┌──────────┐<br>
  │ - color&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
  │ - ruedas&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
  │ - velocidad&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
  └──────────┘<br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;▲<br>
   ┌────┴────┐<br>
   │&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
  Auto&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Moto<br>
  🚗&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;🏍️<br>

##### - Ejemplo: Un control de videojuego
  - El jugador solo ve y usa los botones (interfaz).
  - No necesita saber cómo funciona internamente el circuito del control.




       Joystick
  A - Botón "Saltar"
  B - Botón "Correr"





  




1. [Inicio](README.md) 2. [Anexos](anexos.md)
