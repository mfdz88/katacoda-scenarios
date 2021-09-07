Lo que en actualidad conocemos como "tecnología de contenedores" se remonta al año 2000 como FreeBSD jail, una tecnología que permite 
la partición de un sistema FreeBSD en varios subsistemas o "jaulas" (jails), el cual hace referencia a entornos seguros que un 
administrador de sistemas podía compartir con distintos usuarios dentro o fuera de una empresa.

Para el 2001 se introdujo en Linux la implementación de un entorno aislado por medio del proyecto VServer de Jacques Gélinas. Una vez 
que se estableció para múltiples espacios de usuario controlados en Linux, comenzó a tomar forma lo que hoy es un contenedor de Linux.

Cada vez se combinaron más tecnologías, con mayor rapidez, para hacer realidad este enfoque. Los grupos de control (cgroups) son una 
función del kernel que controla y limita el uso de los recursos para un proceso o grupo de procesos. Además, los cgroups utilizan systemd,
un sistema de inicialización que configura el espacio de usuario y gestiona sus procesos, para proporcionar mayor control de estos procesos 
aislados. Ambas tecnologías, que agregan más control a Linux, también fueron el marco para que los entornos pudieran tener éxito al permanecer separados.

En 2008, Docker apareció en escena con su tecnología de contenedores que lleva el mismo nombre. La tecnología Docker incorporó una serie 
de conceptos y herramientas nuevos: una interfaz de línea de comandos sencilla para ejecutar y diseñar imágenes nuevas en capas, un daemon 
de servidor, una biblioteca de imágenes en contenedores prediseñadas y el concepto de un servidor de registros. Estas tecnologías 
combinadas permitieron que los usuarios diseñaran rápidamente nuevos contenedores en capas y los compartieran con otros sin ninguna dificultad.

Salomon Hykes comenzó Docker comenzó como un proyecto interno dentro de dotCloud, empresa enfocada a PaaS (plataforma como servicio).
Fué liberado como código abierto en marzo de 2013.

