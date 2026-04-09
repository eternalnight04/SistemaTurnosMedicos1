# Anexo - Introducción al Diseño Orientado a Objetos

El paradigma orientado a objetos tiene que ver con visualizar un programa como una serie de objetos que interactuan y tienen relación entre sí, de aquí salen las bases para entender cómo funcionaría cada parte del sistema para luego trasladarlo a código. Es importante ya que sirve para entender mucho mejor cómo funcionaría un sistema complejo dividiendolo en objetos y partes más sencillas y pequeñas.

## Los cuatro fundamentos de POO

- Herencia: Las clases secundarias heredan datos y comportamientos de la clase principal, tal como la clase Cambios hereda datos y comportamientos de la clase Turno (ya que guarda los datos que se modifican ahí)

- Encapsulación: Contiene información de un objeto, exponiendo solo la información seleccionada, tal como funciona la clase Agenda, ya que expone solo la información de los turnos del doctor o profesional seleccionado.

- Abstracción: Define clases simplificando la realidad, ignorando detalles innecesarios y enfocándose en lo que es importante para el programa en particular, esto sucede simplificando todas las clases, como la clase turnos y la clase secretaria, pero es fundamental entender lo importante.

- Polimorfismo: Muchos métodos pueden realizar la misma tarea, esencialmente, los métodos ReservaHorario() y GuardarCambios() de las clases Turno y Agenda hacen lo mismo.


## Requisitos iniciales del sistema

### Requisitos Funcionales

- RF1: Registrar pacientes
- RF2: Asignar turnos
- RF3: Cancelar turnos
- RF4: Reprogramar turnos
- RF5: Ver agenda del médico
- RF6: Evitar superposición de turnos

### Requisitos No Funcionales

- RNF1: Fácil de usar
- RNF2: Respuesta rápida (<2s)
- RNF3: Datos seguros
- RNF4: Disponible en horario laboral
- RNF5: Acceso desde distintos dispositivos


## Casos de uso.

### Caso 1.

-Nombre del caso de uso: Registro de turno.

-Actor involucrado: Paciente u usuario externo.

-Descripción breve: Paciente registra un turno en el sistema.

-Flujo principal de eventos:

      1) Usuario ingresa al sistema.
      2) Pulsa el botón para consultar turnos.
      3) Se muestra un formulario en pantalla de debe rellenar con sus datos y una fecha a escoger en un calendario.
      4) El usuario rellena el formulario y selecciona una fecha y horario concreto.
      5) Se envía el formulario al sistema.
      6) Dentro de poco, recibe una notificación con que su turno ha sido confirmado.

-Precondiciones: Deben haber fechas disponibles para que el paciente pueda elegir.

-Postcondiciones: Se notifica al paciente y al doctor que se registró el turno y este mismo debe aparecer en el calendario, al mismo tiempo que dicho horario del turno tomado ya no debería estar disponible para que otros usuarios puedan escoger.


### Caso 2.

-Nombre del caso de uso: Reprogramación de turno.

-Actores involucrados: Paciente y profesional.

-Descripción breve: El doctor modifica el horario o hace cambios en uno de sus turnos.

-Flujo principal de eventos:

      1) Doctor ingresa al sistema con su nombre de usuario, mail y contraseña.
      2) Pulsa una fecha y horario en el calendario que debe mostrarse a continuación y selecciona "reprogramar turno".
      3) Hace los cambios necesarios.
      4) Guarda los cambios y sale del sistema. El sistema a su vez debe de guardar dichos cambios en un historial en caso de que se 
      quiera acceder a este más tarde.
      5) Los cambios se le son notificados al doctor y al paciente mediante Whatsapp o correo electronico.

-Precondiciones: Debe de haber un turno registrado para que pueda ser modificado.

-Postcondiciones: El turno debe haber sido modificado, se debe haber mandado una notificación a ambas partes de dicho cambio y se debe
registrar este cambios junto con el horario y fecha en que fue realizado en un registro de cambios.


### Caso 3.

-Nombre de caso de uso: Registro de nuevo profesional.

-Actores involucrados: Secretaria.

-Descripción breve: La secretaria agrega un nuevo doctor al sistema para que pueda acceder.

-Flujo principal de eventos:

      1) Ingresa al sistema.
      2) Pulsa un botón para agregar un nuevo usuario para que acceda al sistema.
      3) Se muestra un formulario en pantalla que se debe completar con los datos del nuevo doctor.
      4) Se ingresan los datos y se guardan en el sistema.
      5) El nuevo usuario ingresa y se le pide que cambie la contraseña.
      6) El usuario cambia la contraseña y puede seguir con su sesión.

-Precondiciones: Debe de haber un espacio en el sistema para un nuevo registro.

-Postcondiciones: Se debe de haber registrado un nuevo usuario al sistema como rol de doctor o profesional.


### Caso 4.

-Nombre de caso de uso: Visualización de calendario.

-Actores involucrados: Secretaria.

-Descripción breve: Se debe poder visualizar el calendario en pantalla y tener la posibilidad de imprimirlo. Se puede escoger si solo se
desea ver los turnos que tiene asignado cada doctor o todos los turnos de todos en general.

-Flujo principal de eventos:

      1) Ingreso al sistema.
      2) Pulsa el botón para que se visualice la agenda completa (la idea es que al ingresar, se vea una vista simple de los turnos
      que hay asignados en la semana).
      3) Se escoge que solo se filtren los turnos asignados a un doctor en específico.
      4) Pulsa el botón de imprimir.
      5) Se muestra cómo quedaría impreso.

-Precondiciones: Se debe de haber ingresado en el sistema.

-Postcondiciones: El calendario no debe haber sufrido ningún cambio.

### Caso 5.

-Nombre de caso de uso: Visualización del historial de cambios de turnos.

-Actores involucrados: Secretaria.

-Descripción breve: Se debe poder visualizar el historial de cambios de turnos, con especificaciones de horarios y fechas en que se
realizaron dichas modificaciones y por quien.

-Flujo principal de eventos:

      1) Ingreso al sistema:
      2) Pulsa el botón para que se visualice la agenda completa.
      3) Pulsa el botón para que aparezca el historial de turnos.
      4) Se filtra entre si se quiere visualizar todos los cambios que hubieron en las últimas 24 horas, en toda la semana, en todo el mes
      o en general.
      5) Aparecerá el historial a continuación.

-Precondiciones: Se debe de haber ingresado en el sistema y debe existir un registro de cambios de turnos en el sistema.

-Postcondiciones: El registro no debió haber sufrido ningún cambio luego de la visualización.
