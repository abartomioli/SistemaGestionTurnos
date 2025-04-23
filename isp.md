# Principio de Segregación de Interfaces (ISP)

## Propósito y Tipo del Principio SOLID

El Principio de Segregación de Interfaces (ISP) establece que los clientes no deben estar obligados a depender de interfaces que no utilizan. Es decir, las clases no deberían verse forzadas a implementar métodos que no les competen. Este principio favorece interfaces específicas frente a interfaces generales, promoviendo un diseño más claro, flexible y mantenible.

---

## Motivación

En la versión original, podríamos tener una interfaz genérica IUsuario con métodos como consultarHistorial(), registrarTurno(), cancelarTurno(), confirmarAsistencia() y recibirNotificacion(). Esto obliga a todos los roles (Paciente, Médico, Recepcionista) a implementar o ignorar métodos que no les competen:
 - El Paciente no necesita registrarTurno() ni cancelarTurno().
 - El Recepcionista no necesita consultarHistorial() ni confirmarAsistencia().
 - El Médico no necesita registrarTurno() ni cancelarTurno() ni confirmarAsistencia().
Este acoplamiento innecesario complica el mantenimiento y la evolución de la interfaz.

Ejemplo del mundo real: Imaginá un sistema de gestión de turnos donde todos los usuarios deben implementar una interfaz genérica IUsuario, la cual incluye métodos como registrarTurno(), consultarHistorial(), confirmarAsistencia(), y recibirNotificacion().

Esto sería equivalente a darle a todos los perfiles del sistema (pacientes, médicos y recepcionistas) el mismo panel con todas las funciones disponibles, sin importar si realmente las necesitan o no.

Por ejemplo:
- El Médico no necesita registrar ni cancelar turnos, pero esa interfaz lo obliga a implementar esos métodos, lo cual puede terminar en métodos vacíos o con código innecesario.
- El Paciente no debería confirmar asistencia de otros ni recibir funciones administrativas.
- El Recepcionista no debería consultar el historial clínico de un paciente desde su rol funcional.

Esto es como si en un hospital se les pidiera a todos los empleados que completen el mismo formulario general todos los días, con campos para actividades que no tienen nada que ver con su tarea. Una recepcionista tendría que escribir sobre tratamientos médicos, y un médico sobre llamadas telefónicas o cobro de facturas. No solo sería confuso, sino que generaría errores y frustración.

La solución, aplicando ISP, es dividir esa interfaz en interfaces más específicas como IPaciente, IMedico, IRecepcionista, con los métodos que realmente cada rol necesita. Esto reduce el acoplamiento y mejora la legibilidad, mantenimiento y robustez del sistema.

---

## Aplicación del Principio ISP en las Clases del Proyecto

Para cumplir con el ISP, se pueden definir interfaces específicas y claras para cada tipo de usuario:
Clases que implementan las interfaces:

- Interfaz IHistorial: Solo define la consulta de historial, para Paciente y Médico.
- Interfaz IAgenda: Solo define operaciones de agenda, para Recepcionista.
- Interfaz IAsistencia: Solo define confirmación de asistencia, para Paciente.
- Interfaz INotificable: Solo define recepción de notificaciones, para Paciente y Médico.

Clases que implementaria:
- Paciente implementa IHistorial, IAsistencia, INotificable
- Médico implementa IHistorial, INotificable
- Recepcionista implementa IAgenda
Cada clase depende únicamente de los métodos que realmente utiliza.

Justificación de diseño
- Paciente: puede consultar su historial, confirmar asistencia y recibir notificaciones. No se ve forzado a métodos de agenda.
- Médico: consulta historial y recibe notificaciones de cambios de turno; no registra ni cancela citas.
- Recepcionista: gestiona exclusivamente la creación y cancelación de turnos.
Esta segregación mejora la claridad y facilita añadir nuevas operaciones específicas sin alterar interfaces existentes.

---

## Estructura de Clases (UML)

A continuación se muestra el diagrama UML con la separación de responsabilidades aplicada según el ISP.

![Diagrama UML LSP](diagrama_isp.png)
