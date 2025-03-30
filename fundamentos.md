# Anexo - Los cuatro fundamentos de POO
## Los cuatros fundamentos de POO son:
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

#### 3) Polimorismo
Permite que un mismo método tenga diferentes comportamientos según el contexto.

##### - Ejemplo: Formas de Comunicación
  - Un método enviarmensaje() puede comportarse diferente en un dispositivo.
    - Si es un teléfono, enviará un SMS
    - Si es un WhatsApp, enviará un mensaje de chat.
    - Si es un Correo, enviará un Email.
  - Las subclases "Auto" y "Moto" heredan estos atributos y pueden agregar características propias.

Persona -> enviarMensaje()<br>
   ├──&nbsp; Teléfono&nbsp; 📞&nbsp; →&nbsp; SMS<br>
   ├──&nbsp; WhatsApp&nbsp; 📱&nbsp; →&nbsp; Chat<br>
   ├──&nbsp; Correo&nbsp; ✉&nbsp; →&nbsp; Email<br>


#### 4) Abstracción
Se centra en los aspectos esenciales de un objeto, ocultando detalles innecesarios.

##### - Ejemplo: Un control de videojuego
  - El jugador solo ve y usa los botones (interfaz).
  - No necesita saber cómo funciona internamente el circuito del control.

[🎮 Control de Videojuego]<br>
   ┌──────────────┐<br>
   │  🎚 Joystick&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
   │  🅰 Botón "Saltar"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
   │  🅱 Botón "Correr"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
   └──────────────┘<br>
