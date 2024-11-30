Esta es la parte practica del curso de git de la UPS del 30/11/2024

Para iniciar primero debes realizar un fork de este repositorio en github

En la configuracion del repositorio agregar un valor con la llave integrantes.uno e integrantes.dos con el nombre y apellido de las personas que van a trabajar en este repositorio

Cada uno de los integrantes deben clonarse de forma local el repositorio y realizar los cambios que se indican en este Readme

Agregar a cada persona como colaborador del repositorio en github, en el fork que se crea

Como parte inicial cada persona debe crear un archivo .bin con su nombre y apellido

Luego cada uno debe crear un .gitignore en la rama uno que realice lo siguiente:

Ignorar el archivo claves.txt
Ignorar todos los archivos .pdf
Ignorar directorio de imagenes
Ignorar todos los archivos .log en el directorio de resultados
Ignorar archivo que sea de extension .bin con el nombre y apellido de cada persona

No importa que el resto de  archivos no existan en la rama uno

Realizar un commit con el archivo .gitignore y subirlo al repositorio en la misma rama uno

Esto va a crear un conflicto, deben resolverlo para que acepte todos los cambios y al final cargar todos los cambios al repositorio

Estos cambios se deben actualizar en la rama dos, en este no se incluye el archivo .gitignore (no se deben actualizar los cambios en la rama uno)

En la rama tres se ha hecho un commit con claves, se debe identificar el commit y eliminarlo del historial, para que no se incluyan las claves en el repositorio

En la rama cuatro se debe volver al commit donde se realizó un cambio al archivo archivoD.md, crear un nuevo commit sin estos cambios

Crear una rama con su nombre, esta rama debe salir de la rama cuatro y unirse con los cambios de la rama dos, al final cada uno debe subir su rama al repositorio
