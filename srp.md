# Principio de Responsabilidad Única (SRP)

## Propósito y Tipo del Principio SOLID

El Principio de Responsabilidad Única (Single Responsibility Principle) es un principio de diseño orientado a objetos que establece que una clase debe tener una única razón para cambiar, es decir, debe encargarse de una sola funcionalidad dentro del sistema.

**Tipo de principio**: Principio de diseño de clases.

Este principio ayuda a mantener el código limpio, modular y fácil de mantener. Cuando cada clase tiene una única responsabilidad, se reduce el acoplamiento y se mejora la cohesión. Esto facilita la extensión del sistema y el mantenimiento futuro, ya que los cambios en una funcionalidad no afectan otras partes no relacionadas.

---

## Aplicación del SRP en el Sistema de Gestión de Turnos Médicos

### Clase: `Paciente`

- **Responsabilidad**: Gestionar acciones propias del paciente, como solicitar un turno, confirmar asistencia o consultar su historial.
- **Justificación**: No tiene lógica relacionada con turnos o usuarios en general, se enfoca en su propio comportamiento. Esto mejora la cohesión y permite cambios en la lógica del paciente sin afectar al resto del sistema.

---

### Clase: `Turno`

- **Responsabilidad**: Representar un turno médico, permitiendo modificar su estado o asociarlo a un paciente y médico.
- **Justificación**: No contiene lógica relacionada a la interfaz ni a usuarios. Se centra únicamente en su estado y relaciones. Un cambio en la lógica de estado del turno no afecta al paciente o al sistema.

---

### Clase: `Sistema`

- **Responsabilidad**: Funcionar como orquestador general, mostrando historiales, verificando disponibilidad de turnos y enviando notificaciones.
- **Justificación**: Separa claramente sus responsabilidades de las de los actores (Paciente, Médico, Recepcionista). Permite modificar el sistema de notificaciones, por ejemplo, sin alterar las clases de usuario.

---

## Conclusión

La aplicación del Principio de Responsabilidad Única permite que las clases del sistema estén organizadas de forma coherente y mantenible. Al tener responsabilidades bien definidas y separadas, se favorece la reutilización, el testeo y la evolución del sistema de forma segura.
