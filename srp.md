# Principio de Responsabilidad Única (SRP)

## Propósito y Tipo del Principio SOLID

El Principio de Responsabilidad Única (Single Responsibility Principle) indica que una clase debe tener una única razón para cambiar, es decir, debe tener una única responsabilidad dentro del sistema. Este es un **principio de diseño de clases** que promueve una estructura de código modular, fácil de mantener y escalar.

Aplicando este principio, las clases evitan mezclar diferentes lógicas de negocio, lo que facilita su comprensión y reduce la posibilidad de errores al modificar una funcionalidad específica.

---

## Motivación

En nuestro sistema de gestión de turnos médicos, la clase SISTEMA concentraba:
- Búsqueda de disponibilidad de turnos.
- Envío de notificaciones (e‑mail, SMS, WhatsApp).
- Actualización del historial de citas.
- Acceso directo a la base de datos de horarios.
Esta mezcla de responsabilidades implicaba que cualquier cambio en la lógica de notificaciones (por ejemplo, migrar de e‑mail a WhatsApp) obligaba a modificar Sistema, arriesgando romper funcionalidades de búsqueda o de historial.
Aplicar SRP nos lleva a extraer cada responsabilidad en servicios dedicados, de modo que:
1) Cambios en la lógica de búsqueda de horarios no afecten al envío de mensajes.
2) Variaciones en la política de auditoría se aíslen en un componente propio.
3) El acceso a datos se maneje por repositorios especializados.
**Ejemplo del mundo real:**  
Pensemos en una impresora multifunción. Si una sola clase maneja impresión, escaneo y envío de fax, cualquier cambio en la funcionalidad de escaneo podría afectar la impresión, aunque no estén directamente relacionadas. Aplicar SRP implicaría separar esas funcionalidades en clases distintas como `Impresora`, `Escáner` y `Fax`, cada una con su única responsabilidad.

---

## Aplicación del Principio SRP en las Clases del Proyecto

### Clase: `Paciente`
- **Responsabilidad única**: Gestionar los datos del paciente y su historial de turnos.
- **Mejora**: Se evita que tenga lógica de gestión de turnos o notificaciones, que ahora corresponde al `Sistema`.

### Clase: `Turno`
- **Responsabilidad única**: Administrar el estado y la asignación de un turno.
- **Mejora**: No tiene lógica de envío de mensajes o validaciones externas.

### Clase: `Sistema`
- **Responsabilidad única**: Coordinar funcionalidades del sistema, como búsquedas, notificaciones y visualización de datos.
- **Mejora**: Centraliza tareas de coordinación, sin apropiarse de responsabilidades específicas de los actores del sistema.

---

## Estructura de Clases (UML)

A continuación se muestra el diagrama UML con la separación de responsabilidades aplicada según el SRP.

![Diagrama UML SRP](diagrama_srp.png)
