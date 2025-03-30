# Casos de Uso:

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




1. [Inicio](README.md) 2. [Anexos](anexos.md) 3. [Fundamentos POO](fundamentos.md) 4. [Requisitos](requisitos.md) 5. [Introduccion](introduccion.md)
