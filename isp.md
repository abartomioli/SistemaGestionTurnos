# Principio de Segregación de Interfaces (ISP)

## Propósito y Tipo del Principio SOLID

El Principio de Segregación de Interfaces (ISP) establece que los clientes no deben estar obligados a depender de interfaces que no utilizan. Es decir, las clases no deberían verse forzadas a implementar métodos que no les competen. Este principio favorece interfaces específicas frente a interfaces generales, promoviendo un diseño más claro, flexible y mantenible.
---

## Motivación

En el sistema original, las clases Paciente, Médico y Recepcionista heredan directamente de una clase base común (Usuario). Esta clase Usuario, si estuviera mal diseñada, podría contener métodos genéricos como consultarHistorial, registrarTurno, cancelarTurno, etc., que no aplican de igual manera para todos los tipos de usuario.
Esto obligaría a clases como Médico o Recepcionista a implementar o ignorar métodos que no necesitan, violando así el ISP.

Ejemplo del mundo real: Imaginá que todos los empleados de un hospital tuvieran que llenar el mismo formulario para reportar sus tareas. Una enfermera tendría que escribir sobre turnos de cirugía y un recepcionista sobre medicación, cosas que no tienen sentido para su rol. Lo ideal sería que cada uno reciba un formulario con campos específicos para su función.

---

## Aplicación del Principio LSP en las Clases del Proyecto

Para cumplir con el ISP, se pueden definir interfaces específicas y claras para cada tipo de usuario:
Clases que implementan las interfaces:

- Paciente:
   Implementa: IHistorial, IAsistencia, INotificable
   Justificación: puede consultar su historial, confirmar asistencia y recibir notificaciones.

- Médico:
   Implementa: IHistorial, INotificable
   Justificación: puede consultar su agenda de turnos y recibir alertas.

- Recepcionista:
   Implementa: IAgenda
   Justificación: se encarga exclusivamente de registrar o cancelar turnos.

---

## Estructura de Clases (UML)

A continuación se muestra el diagrama UML con la separación de responsabilidades aplicada según el ISP.

![Diagrama UML LSP](diagrama_isp.png)
