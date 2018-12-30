# QuitarMemoriaEnStandBy
Utilidad para poder quitar tartamudeo en juegos por la memoria en espera.

En Windows 10 Creators Update Hay un problema de tartamudeos con la memoria en espera, esto recibe un gran golpe de rendimiento al llenarse. esta es la forma de solucionarlo permanente.

esto no sucedia en Win10 1607
la solucion permanente es:

Esto arregla el tartamudeo en el sistema (o stuttering).

Descargue EmptyStandbyList y colóquelo en un lugar donde no lo mueva https://wj32.org/wp/software/empty-standby-list/
posiblemente cree una carpeta en "archivos de programa".

Haga clic derecho -> Propiedades y seleccione "Ejecutar como administrador".

Abra el Programador de tareas -> Crear tarea en el extremo derecho

General -> (asígnar un nombre). En Opciones de seguridad -> Cambiar usuario o grupo -> Avanzado -> Buscar ahora -> vaya abajo y elija SISTEMA (importante para que se ejecute silenciosamente en segundo plano). Marque 'Ejecutar con privilegios más altos' y 'Oculto' en la parte inferior. ejemplo aquí https://stackoverflow.com/questions/6568736/how-do-i-set-a-windows-scheduled-task-to-run-in-the-background

Pestaña Desencadenadores -> Nuevo -> Segun una programación -> Marque la tarea de repetición cada 5 minutos.
Elejir durante 'indefinidamente'

Pestaña Acciones -> Nueva -> iniciar un programa -> Programa o Script: (seleccionar "EmptyStandByList.exe")

biblioteca del programador de tareas -> Seleccionar el nombre de la tarea (ejemplo "EmptyStandByList") -> Ejecutar

Listo La memoria de espera se borra automáticamente cada 5 minutos.
