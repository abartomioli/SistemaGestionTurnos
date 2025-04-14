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


## Anexo - Requisitos Iniciales del Sistema

1️⃣ Gestión de Turnos:
    El sistema debe permitir el registro, modificación y cancelación de turnos por parte del personal autorizado.
    Debe validar que un médico no tenga más turnos de los que puede atender en su horario de trabajo.

2️⃣ Historial de Turnos:
    Se debe almacenar el historial de turnos de cada paciente, incluyendo fecha, médico, especialidad y estado del turno.
    El paciente podrá consultar su historial de turnos a través de una interfaz web o móvil.

3️⃣ Notificaciones Automáticas:
    El sistema debe enviar confirmaciones, cancelaciones y modificaciones de turnos a los pacientes y médicos vía email o SMS.
    Se debe permitir la confirmación automática por parte del paciente a través de un enlace en la notificación.

4️⃣ Gestión de Pacientes y Profesionales:
    Debe permitir el registro, edición y consulta de pacientes y profesionales de la salud.
    Solo personal autorizado podrá acceder a la información de contacto de los pacientes y médicos.

5️⃣ Control de Acceso y Seguridad:
    El sistema debe contar con roles y permisos para restringir el acceso a la información sensible.
    Solo el personal autorizado podrá modificar turnos o acceder a datos de pacientes.

## Anexo - Casos de Uso

## 📌 Caso de Uso 1: Registrar un Turno<br>
Nombre: Registrar Turno<br> 
Actor: Recepcionista / Paciente (si hay autogestión)<br>
Descripción: Permite registrar un nuevo turno para un paciente con un médico en una fecha y hora determinada.<br>
Precondiciones:<br>
- El paciente debe estar registrado en el sistema.<br>
- El médico debe tener disponibilidad en su horario.<br>
  
### Flujo Principal:<br>
1. El actor accede al módulo de gestión de turnos.<br>
2. Ingresa los datos del paciente y selecciona la especialidad.<br>
3. El sistema muestra la disponibilidad de médicos y horarios.<br>
4. El actor selecciona un médico y un horario disponible.<br>
5. Se ingresa el motivo de la consulta y observaciones (si es necesario).<br>
6. Se confirma la reserva del turno.<br>
7. El sistema registra el turno y envía una notificación de confirmación.<br>

#### Postcondición:<br>
- El turno queda registrado en el historial del paciente y del médico.<br>
<br>
<br>


## 📌 Caso de Uso 2: Cancelar un Turno<br>
Nombre: Cancelar Turno<br>
Actor: Paciente / Recepcionista<br>
Descripción: Permite cancelar un turno previamente agendado.<br>
Precondiciones:<br>
- El turno debe estar registrado en el sistema.<br>

### Flujo Principal:<br>
1. El actor accede a la lista de turnos asignados.<br>
2. Busca el turno a cancelar.<br>
3. Confirma la cancelación del turno.<br>
4. El sistema actualiza el estado del turno a "Cancelado".<br>
5. Se notifica al paciente y al médico sobre la cancelación.<br>

#### Postcondición:<br>
- El turno queda registrado como cancelado en el sistema.<br>
<br>
<br>


## 📌 Caso de Uso 3: Confirmar Asistencia a un Turno<br>
Nombre: Confirmar Turno<br>
Actor: Paciente<br>
Descripción: Permite que el paciente confirme su asistencia a un turno.<br>
Precondiciones:<br>
- El turno debe estar en estado "Pendiente".<br>

### Flujo Principal:<br>
1. El sistema envía una notificación con un enlace de confirmación.<br>
2. El paciente accede al enlace y confirma su asistencia.<br>
3. El sistema cambia el estado del turno a "Confirmado".<br>
4. Se notifica al médico sobre la confirmación.<br>

#### Postcondición:<br>
- El turno queda registrado como "Confirmado".<br>
<br>
<br>


## 📌 Caso de Uso 4: Consultar Historial de Turnos<br>
Nombre: Consultar Historial de Turnos<br>
Actor: Paciente / Médico / Recepcionista<br>
Descripción: Permite visualizar el historial de turnos de un paciente o médico.<br>
Precondiciones:<br>
- El usuario debe tener permisos para consultar el historial.<br>

### Flujo Principal:<br>
1. El actor accede al sistema con sus credenciales.<br>
2. Busca el historial de turnos de un paciente o médico.<br>
3. El sistema muestra la lista de turnos con su estado (Confirmado, Cancelado, Pendiente, Atendido).<br>
4. Se pueden aplicar filtros por fechas y especialidad.<br>

#### Postcondición:<br>
- Se obtiene la información del historial de turnos.<br>
<br>
<br>


## 📌 Caso de Uso 5: Registrar un Paciente<br>
Nombre: Registrar Paciente<br>
Actor: Recepcionista<br>
Descripción: Permite registrar un nuevo paciente en el sistema.<br>
Precondiciones:<br>
- El paciente no debe estar registrado previamente.<br>

### Flujo Principal:<br>
1. El actor accede al módulo de pacientes.<br>
2. Ingresa los datos personales del paciente (Nombre, DNI, Fecha de Nacimiento, Teléfono, Email).<br>
3. El sistema verifica que el paciente no esté duplicado.<br>
4. Se confirma el registro del paciente.<br>
5. El sistema almacena la información en la base de datos.<br>

#### Postcondición:<br>

El paciente queda registrado y disponible para asignación de turnos.<br>


## Anexo - Boceto Inicial del diseño de clases

[Diagrama de Clases - SISTUR](https://github.com/abartomioli/SistemaGestionTurnos/blob/main/diagramaClases.jpg?raw=true)



