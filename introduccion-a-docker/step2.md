Como se ha mencionado anterior mente, Docker es un proyecto de código abierto que permite automatizar el 
despliegue de aplicaciones dentro de “contenedores”. Un  contenedor empaqueta todo lo necesario para que 
uno o más procesos (servicios o aplicaciones) funcionen: código, herramientas del sistema, bibliotecas 
del sistema, dependencias,etc. Ésto garantiza que siempre se podrá ejecutar, independientemente del entorno 
en el que queramos desplegarlo. No hay que preocuparse de qué software ni versiones tiene nuestra máquina,
ya que nuestra aplicación se ejecutará en el contenedor.


<h3>¿Que es docker ?</h3>

Docker  permite ejecutar contenedores. Un contenedor es un proceso de espacio aislado que ejecuta una 
aplicación y sus dependencias en el sistema operativo host. La aplicación dentro del contenedor se 
considera a sí misma como el único proceso que se ejecuta en la máquina, mientras que la máquina puede 
ejecutar varios contenedores de forma independiente.

"Es una pieza de software liviana, independiente, empaquetable y ejecutable que incluye todo lo que 
necesita para correr: código, runtime, herramientas de sistema, librerías y configuraciones"(.docker.com,2021)

Las principales características de Docker son:

• Portabilidad: el contenedor Docker podemos desplegarlo en cualquier sistema, sin
necesidad de volver a configurarlo o realizar las instalaciones necesarias para que la
aplicación funcione, ya que todas las dependencias son empaquetadas con la aplicación en el
contenedor.

• Ligereza: los contenedores Docker sólo contienen lo que las diferencia del sistema operativo
en el que se ejecutan, no se virtualiza un SO completo.
• Autosuficiencia: un contenedor Docker no contiene todo un sistema operativo completo,
sólo aquellas librerías, archivos y configuraciones necesarias para desplegar las
funcionalidades que contenga.

Ya tenemos instalado Docker en nuestra máquina anfitriona cuyo SO es Ubuntu 14.04 LTS.
Si escribimos “docker version” en la línea de comandos, nos da la versión del cliente y del
servidor, además de la versión de la API y de Go (lenguaje de programación en el que está escrito
Docker).

`docker version`{{execute}}