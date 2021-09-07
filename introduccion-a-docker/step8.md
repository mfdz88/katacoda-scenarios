DOCKERHUB
sirve como repositorio de
imágenes oficiales y de terceros.
Las características de Docker Hub son:
• Repositorios de imágenes: encuentra, administra, sube y descarga imágenes oficiales y de la
comunidad.
• Imágenes automáticas: crea nuevas imágenes cuando haces un cambio en la fuente de
Github o BitBucket.

LINKS
Para que dos contenedores colaboren entre ellos podemos abrir puertos y que se comuniquen
por ahí, pero Docker nos ofrece la posibilidad de crear links entre contenedores


VOLÚMENES
Podemos montar volúmenes de datos en nuestros contenedores. Con el flag -v podemos
montar un directorio dentro de nuestro contenedor. Así podemos incorporar datos que estarían
disponibles para nuestro contenedor. Además seguirá apareciendo después de un reinicio del
contenedor, serán persistentes.
También podemos compartir volúmenes de datos entre contenedores. Si dichos volúmenes
están anclados al sistema operativo anfitrión, no serán eliminados por Docker cuando desaparezca
el contenedor.

CONFIGURACIÓN DE RED
Por defecto los contenedores tienen las conexiones de redes habilitadas


KUBERNETES
Es un proyecto open source de Google para la gestión de aplicaciones en contenedores, en
especial los contenedores Docker, permitiendo programar el despliegue, escalado, monitorización
de los contenedores, etc.
A pesar de estar diseñado para contenedores Docker, Kubernetes puede supervisar
servidores de la competencia como Amazon o Rackspace.
Permite empaquetar las aplicaciones en contenedores y trasladarlos fácil y rápidamente a
cualquier equipo para ejecutarlas.
Kubernetes es similar a Docker Swarm, que es la herramienta nativa de Docker para
construir un clúster de máquinas. Fue diseñado para ser un entorno para la creación de aplicaciones
distribuidas en contenedores. Es un sistema para la construcción, funcionamiento y gestión de
sistemas distribuidos.