Lo que en actualidad conocemos como "tecnología de contenedores" se remonta al año 2000 con <b>FreeBSD jail</b>, una tecnología que permite 
la partición de un sistema FreeBSD en varios subsistemas o "jaulas" (jails), el cual hace referencia a entornos seguros o <b>Sanbox</b> que un 
administrador de sistemas podía compartir con distintos usuarios dentro o fuera de una empresa.

Para el 2001 se introdujo la implementación de un entorno aislado en Linux por medio del proyecto VServer de Jacques Gélinas. Una vez 
que se estableció para múltiples espacios de usuario controlados en Linux, comenzó a tomar forma lo que hoy es un contenedor de Linux.

Cada vez se combinaron más tecnologías, con mayor rapidez, para hacer realidad este enfoque. En 2008, Docker apareció en escena con su 
tecnología de contenedores que lleva el mismo nombre. La tecnología Docker incorporó una serie de conceptos y herramientas nuevos: una 
interfaz de línea de comandos sencilla para ejecutar y diseñar imágenes nuevas en capas, un daemon de servidor, una biblioteca de imágenes 
en contenedores prediseñadas y el concepto de un servidor de registros. Estas tecnologías combinadas permitieron que los usuarios diseñaran 
rápidamente nuevos contenedores en capas y los compartieran con otros sin ninguna dificultad. En marzo de 2013 fué liberado Docker como código abierto.

<h3>Diferencias entre contenedor y virtualizacion</h3>

"Las máquinas virtuales (VM) y los contenedores de Linux son entornos informáticos empaquetados que combinan varios elementos de TI y los aíslan del resto del sistema. Las principales diferencias radican en la capacidad de ampliación y la portabilidad." (redhat.com,2021)

    Por lo general, los contenedores se miden en megabytes. El elemento más grande que empaquetan es una aplicación y todos los archivos necesarios para su ejecución. También suelen utilizarse para empaquetar funciones individuales que realizan tareas específicas (conocidas como microservicios). La naturaleza ligera de los contenedores y su sistema operativo (SO) compartido permiten trasladarlos entre los distintos entornos con mucha facilidad.
	
    Por lo general, las máquinas virtuales se miden en gigabytes. Suelen tener su propio sistema operativo, lo cual les permite realizar varias funciones con uso intensivo de los recursos al mismo tiempo. Las máquinas virtuales cuentan con una mayor cantidad de recursos disponibles, lo que les permite extraer, dividir, duplicar y simular sistemas operativos, escritorios, bases de datos, conexiones de red y servidores completos. 
	
<h4>Virtualización</h4>

El software llamado hipervisor separa los recursos de las máquinas físicas para que puedan dividirse y destinarse a las máquinas virtuales. Cuando un usuario emite una instrucción de una máquina virtual que requiere recursos adicionales del entorno físico, el hipervisor transmite la solicitud al sistema físico y almacena los cambios en la memoria caché. Las máquinas virtuales parecen servidores físicos y actúan como tales, lo que puede multiplicar las desventajas de las dependencias de las aplicaciones y los grandes footprints del sistema operativo. Incluso, en la mayoría de los casos, ese footprint no se necesita para ejecutar una sola aplicación o microservicio.

<h4>Contenedores</h4>

Los contenedores contienen un microservicio o una aplicación y todo lo que necesita para ejecutarse. Lo que está dentro de un contenedor se conserva en lo que llamamos imagen: un archivo basado en un código que incluye todas las bibliotecas y las dependencias. Estos archivos pueden considerarse una instalación de la distribución de Linux, porque la imagen viene con paquetes RPM y archivos de configuración. Como los contenedores son tan pequeños, suele haber cientos de ellos con un nivel de acoplamiento bajo, así que se utilizan plataformas de organización de contenedores (como Red Hat OpenShift y Kubernetes) para configurarlos y gestionarlos.
	
https://youtu.be/ZQlQumDZ0Zw

Referencias : 
