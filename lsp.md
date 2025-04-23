# Principio de Sustitución de Liskov (LSP)

## Propósito y Tipo del Principio SOLID

El Principio de Sustitución de Liskov (LSP) establece que una clase derivada debe poder sustituir a su clase base sin alterar el comportamiento esperado del programa. Es un principio de herencia y comportamiento polimórfico, que asegura la coherencia funcional entre superclases y subclases.
En nuestro sistema de turnos médicos, aplicamos este principio asegurando que las clases derivadas como Paciente, Médico y Recepcionista puedan usarse en cualquier contexto donde se espera un Usuario, sin romper la lógica del sistema.

---

## Motivación

Inicialmente, la clase Usuario se utilizaba como clase base, pero al incorporar funciones específicas para Paciente (como consultar su historial) o Recepcionista (como registrar un turno), se volvió necesario extenderla adecuadamente.

El problema surgía cuando métodos definidos en la clase base no eran aplicables a todas las subclases, lo cual violaba el contrato esperado. Por ejemplo, si Recepcionista heredaba un método consultarHistorial() de Usuario pero no lo utilizaba, el sistema podría arrojar errores o tener un comportamiento inconsistente.

Ejemplo del mundo real
Imaginemos que la clase Usuario tiene un método registrarTurno(). Si todas las subclases (Paciente, Médico, Recepcionista) heredan este método, estaríamos asumiendo que cualquier tipo de usuario puede registrar un turno. Sin embargo, esto no es cierto: solo los pacientes y recepcionistas deberían tener esa responsabilidad.
Si el sistema permitiera que un Médico acceda a registrarTurno() simplemente porque hereda de Usuario, estaríamos violando el principio de sustitución de Liskov. El sistema fallaría en tiempo de ejecución o generaría confusión, porque la subclase estaría usando un método que conceptualmente no le corresponde.
Para resolverlo, dividimos las responsabilidades en clases derivadas específicas que implementan interfaces adecuadas o tienen solo los métodos que realmente necesitan, asegurando que cada subclase respete el contrato de su clase base.

---

## Aplicación del Principio LSP en las Clases del Proyecto

Para cumplir con LSP:
Se creó una jerarquía clara donde Usuario define solo métodos comunes.
Las subclases (Paciente, Médico, Recepcionista) implementan sus propios métodos sin alterar la lógica de Usuario.
Cada instancia de una subclase puede usarse como Usuario sin producir errores inesperados.

---

## Estructura de Clases (UML)

A continuación se muestra el diagrama UML con la separación de responsabilidades aplicada según el LSP.

![Diagrama UML LSP](diagrama_lsp.png)
