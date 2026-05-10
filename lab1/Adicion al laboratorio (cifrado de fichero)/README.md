Como adición al primer laboratorio se implementara cifrado a un fichero

¿QUE SE HARA?
Se creara un fichero con datos sensibles el cual luego será cifrado mediante gpg. Una vez cifrado se podrá ver que el archivo no puede ser leído y que para proceder a leerlo se deberá de descifrar el fichero mediante una contraseña que es colocada cuando el proceso de cifrado se llevo a cabo

¿QUE SE VERA?
-La creación y el cifrado de un fichero
-Como se cifra un fichero
-Que es lo que se ve al tratar de leer un fichero cifrado
-Como leer un  fichero que esta cifrado

FINALIDAD
Verificar la función de cifrado con la que cuenta ubuntu para darle una capa de protección a los archivos que pueden estar en un equipo para la protección de información sensible. Esto demuestra que el cifrado de archivo es muy importante ya que agrega una capa de seguridad a los archivos que creemos no solo impidiendo que un posible atacante lea los datos si obtiene el fichero sino que también impidiéndole el ingreso mediante una contraseña.

HERRAMIENTAS
Ubuntu server
gpg 

DESARROLLO
Primero se crea el fichero con nano
<img src="images/1creacion-fichero.png" alt="Creación del fichero">

Luego se añaden los datos
<img src="images/2datos-fichero.png" alt="Datos">

Con los datos ya ingresados se realiza el cifrado con gpg el cual es una herramienta de cifrado que viene por defecto en ubuntu server, esta herramienta realiza el cifrado mediante algoritmos criptograficos 
<img src="images/3cifrado.png" alt="Cifrado">

Luego de ingresar el comando para cifrar el fichero se nos pedira colocar una contraseña
<img src="images/4password.png" alt="password">

<img src="images/5ingreso-password.png" alt="ingreso password">

Mediante un ls se puede verificar que con el proceso de cifrado ya terminado al archivo que ciframos se le añade la extension .gpg
<img src="images/6se-agrega-extensiongpg.png" alt="extension">

Para verificar si el cifrado fue exitoso se intenta ingresar a el y leerlo con el comando cat
<img src="images/7no-se-leen-datos.png" alt="intento de ingreso">

Como se puede ver los datos no pueden ser leidos solo se pueden visualizar binarios por lo tanto, los datos estan protegidos.

Para poder leer los datos se debe ingresar el siguiente comando

<img src="images/8ver-fichero-cifrado.png" alt="lectura archivo cifrado">

Con este comando ingresado se nos pedira la contraseña la cual definimos anteriormente

<img src="images/9peticion-password.png" alt="password">

Cuando la contraseña es colocada con exito se pueden visualizar los datos correctamente

<img src="images/10lectura-fichero-cifrado.png" alt="lectura de datos">

Cuando se ingresa una contraseña incorrecta el fichero no podra ser leido

<img src="images/11password-incorrecta.png" alt="lectura fallida">
