Requisitos funcionales.
1) El sistema debe permitir crear, reprogramar y cancelar turnos de manera digital.
2) Debe de tener una agenda con visualizacion clara y facil de entender de los turnos por dia y semana (se podría asignar un color
diferente para cada doctor así se puede ver mejor de manera rápida.)
3) El sistema debe de enviar recordatorios al paciente, ya sea por Whatsapp o correo electronico, del turno o de cambios que se hayan hecho
al mismo. Los recordatorios deben ser 24 horas antes del horario del turno.
4) No se pueden permitir turnos que caigan en vacaciones, feriados o simplemente ocasiones donde el doctor no pueda estar disponible
por una u otra razón.
5) Poder registrar si el paciente llegó al turno especificando la hora o si aún sigue en la sala de espera, no se debe cancelar el turno
automáticamente si el paciente todavía no llegó al consultorio, a veces se tienen consideraciones.

Requisitos no funcionales:
1) El sistema debe ser simple de entender y manejar, no debe tener nada complicado, se busca que sea comodo de manejar para todo
tipo de personas.
2) El sistema debe ser capaz de actualizarse, ya sea para agregar nuevos profesionales o para agregar historias clínicas. En resumen,
se debe poder modificar y agregar nuevas cosas sin que se modifique el diseño base.
3) El sistema no debe permitir sobreturnos a menos que el profesional a cargo lo habilite, y para este tipo de casos se deberá implementar
y guardar un historial de cambios.
4) El MVP debe funcionar para principios de julio.
5) El sistema debe ser seguro para que ningún otro usuario más que la secretaria o los doctores puedan modificar algo.

---------------------------------

Casos de uso.

Caso 1.

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
-Postcondiciones: Se notifica al paciente y al doctor que se registró el turno y este mismo debe aparecer en el calendario, al mismo tiempo
                  que dicho horario del turno tomado ya no debería estar disponible para que otros usuarios puedan escoger.

Caso 2.

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

Caso 3.

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

Caso 4.

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

Caso 5.

-Nombre de caso de uso: Visualización del historial de cambios de turnos.
-Actores involucrados: Secretaria.
-Descripción breve: Se debe poder visualizar el historial de cambios de turnos, con especificaciones de horarios y fechas en que se
realizaron dichas modificaciones y por quien.
-Flujo principal de eventos:
      1) Ingreso al sistema:
      2) Pulsa el botón para que se visualice la agenda completa.
      3) 
