# Anexo - Principios SOLID

Los principios SOLID son un conjunto de buenas prácticas para el diseño de software orientado a objetos, cuyo objetivo es crear sistemas más comprensibles, flexibles y mantenibles. Cada principio aborda un aspecto particular del diseño, ayudando a reducir la dependencia entre componentes, facilitar la extensión de funcionalidades y mejorar la reutilización del código.

- [Responsabilidad Única (SRP)](srp.md)
Cada clase debe tener una única razón para cambiar, es decir, una sola responsabilidad o función en el sistema. Esto favorece la cohesión y reduce el acoplamiento.

- [Abierto/Cerrado (OCP)](ocp.md)
Las clases deben estar abiertas a la extensión pero cerradas a la modificación. Esto permite añadir nuevas funcionalidades sin alterar el código existente, promoviendo la estabilidad y escalabilidad.

- [Sustitución de Liskov (OCP)](lsp.md)
Las subclases deben ser sustituibles por sus clases base sin alterar el comportamiento esperado del sistema. Garantiza que las jerarquías de herencia sean coherentes y funcionales.

- [Segregación de Interfaces (ISP)](isp.md)
Los clientes no deberían depender de interfaces que no utilizan. Es preferible tener muchas interfaces específicas en lugar de una sola interfaz general con muchas operaciones.

- [Inversión de Dependencias (DIP)](dip.md)
Las clases de alto nivel no deben depender de clases de bajo nivel, sino de abstracciones. Este principio desacopla los módulos del sistema, facilitando el mantenimiento y las pruebas.
