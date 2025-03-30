# Casos de Uso:

📌 Caso de Uso 1: Registrar un Turno
Nombre: Registrar Turno 
Actor: Recepcionista / Paciente (si hay autogestión)
Descripción: Permite registrar un nuevo turno para un paciente con un médico en una fecha y hora determinada.
Precondiciones:

El paciente debe estar registrado en el sistema.

El médico debe tener disponibilidad en su horario.
Flujo Principal:

El actor accede al módulo de gestión de turnos.

Ingresa los datos del paciente y selecciona la especialidad.

El sistema muestra la disponibilidad de médicos y horarios.

El actor selecciona un médico y un horario disponible.

Se ingresa el motivo de la consulta y observaciones (si es necesario).

Se confirma la reserva del turno.

El sistema registra el turno y envía una notificación de confirmación.
Postcondición:

El turno queda registrado en el historial del paciente y del médico.

📌 Caso de Uso 2: Cancelar un Turno
Nombre: Cancelar Turno
Actor: Paciente / Recepcionista
Descripción: Permite cancelar un turno previamente agendado.
Precondiciones:

El turno debe estar registrado en el sistema.
Flujo Principal:

El actor accede a la lista de turnos asignados.

Busca el turno a cancelar.

Confirma la cancelación del turno.

El sistema actualiza el estado del turno a "Cancelado".

Se notifica al paciente y al médico sobre la cancelación.
Postcondición:

El turno queda registrado como cancelado en el sistema.

📌 Caso de Uso 3: Confirmar Asistencia a un Turno
Nombre: Confirmar Turno
Actor: Paciente
Descripción: Permite que el paciente confirme su asistencia a un turno.
Precondiciones:

El turno debe estar en estado "Pendiente".
Flujo Principal:

El sistema envía una notificación con un enlace de confirmación.

El paciente accede al enlace y confirma su asistencia.

El sistema cambia el estado del turno a "Confirmado".

Se notifica al médico sobre la confirmación.
Postcondición:

El turno queda registrado como "Confirmado".

📌 Caso de Uso 4: Consultar Historial de Turnos
Nombre: Consultar Historial de Turnos
Actor: Paciente / Médico / Recepcionista
Descripción: Permite visualizar el historial de turnos de un paciente o médico.
Precondiciones:

El usuario debe tener permisos para consultar el historial.
Flujo Principal:

El actor accede al sistema con sus credenciales.

Busca el historial de turnos de un paciente o médico.

El sistema muestra la lista de turnos con su estado (Confirmado, Cancelado, Pendiente, Atendido).

Se pueden aplicar filtros por fechas y especialidad.
Postcondición:

Se obtiene la información del historial de turnos.

📌 Caso de Uso 5: Registrar un Paciente
Nombre: Registrar Paciente
Actor: Recepcionista
Descripción: Permite registrar un nuevo paciente en el sistema.
Precondiciones:

El paciente no debe estar registrado previamente.
Flujo Principal:

El actor accede al módulo de pacientes.

Ingresa los datos personales del paciente (Nombre, DNI, Fecha de Nacimiento, Teléfono, Email).

El sistema verifica que el paciente no esté duplicado.

Se confirma el registro del paciente.

El sistema almacena la información en la base de datos.
Postcondición:

El paciente queda registrado y disponible para asignación de turnos.




1. [Inicio](README.md) 2. [Anexos](anexos.md) 3. [Fundamentos POO](fundamentos.md) 4. [Requisitos](requisitos.md) 5. [Casos de Uso](casoUso.md)
