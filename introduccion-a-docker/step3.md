
Docker usa una arquitectura cliente-servidor. El cliente de Docker habla con el demonio de
Docker que hace el trabajo de crear, correr y distribuir los contenedores. Ambos pueden ejecutarse
en el mismo sistema, o se puede conectar un cliente a un demonio Docker remoto. El cliente Docker
y el demonio se comunican vía sockets o a través de una RESTfull API. (imagen pagina oficial).
Explicamos un poco por orden la arquitectura o funcionamiento de Docker:
El cliente de Docker (Docker Client) es la principal interfaz de usuario para Docker. Él
acepta comandos del usuario y se comunica con el demonio Docker.
El demonio Docker (Docker Engine) corre en una máquina anfitriona (host). El usuario no
interactúa directamente con el demonio, en su lugar lo hace a través del cliente Docker.

El demonio Docker levanta los contenedores haciendo uso de las imágenes, que pueden
estar en local o en el Docker Registry.
Cada contenedor se crea a partir de una imagen y es un entorno aislado y seguro dónde se
ejecuta nuestra aplicación.

<h4>Componentes</h4>

Según la documentación oficial, Docker tiene dos principales componentes:

• Docker
Plataforma open source de virtualización con contenedores.
• Docker Hub
Plataforma de Software como servicio (SaaS, Software-as-a-Service) para compartir y
administrar contenedores Docker.

Pero también necesitamos conocer otros componentes y conceptos:

• Docker Engine
Es el demonio que se ejecuta dentro del sistema operativo (Linux) y que expone una API
para la gestión de imágenes, contenedores, volúmenes o redes. Sus funciones principales son:
- La creación de imágenes Docker.
- Publicación de imágenes en Docker Registry.
- Descarga de imágenes desde Docker Registry.
- Ejecución de contenedores usando las imágenes.
- Gestión de contenedores en ejecución (pararlo, arrancarlo, ver logs, ver estadísticas).

• Docker Client
Cualquier software o herramienta que hace uso de la API del demonio Docker, pero suele
ser el comando docker, que es la herramienta de línea de comandos para gestionar Docker Engine.
Éste cliente puede configurarse para hablar con un Docker local o remoto, lo que permite
administrar nuestro entorno de desarrollo local como nuestros servidores de producción.

• Docker Images
Son plantillas de sólo lectura que contienen el sistema operativo base (más adelante
entraremos en profundidad) dónde correrá nuestra aplicación, además de las dependencias y
software adicional instalado, necesario para que la aplicación funcione correctamente. Las plantillas
son usadas por Docker Engine para crear los contenedores Docker.

• Docker Registries
Los registros de Docker guardan las imágenes. Pueden ser repositorios públicos o privados.
El registro público lo provee el Hub de Docker, que sirve tanto imágenes oficiales cómo las subidas
por usuarios con sus propias aplicaciones y configuraciones.
Así tenemos disponibles para todos los usuarios imágenes oficiales de las principales
aplicaciones (MySQL, MongoDB, Apache, Tomcat, etc.), así cómo no oficiales de infinidad de
aplicaciones y configuraciones.
DockerHub ha supuesto una gran manera de distribuir las aplicaciones. Es un proyecto open
source que puede ser instalado en cualquier servidor. Además nos ofrecen un sistema SaaS de pago.

• Docker Containers
El contenedor de Docker aloja todo lo necesario para ejecutar un servicio o aplicación. Cada
contenedor es creado de una imagen base y es una plataforma aislada.
Un contenedor es simplemente un proceso para el sistema operativo, que se aprovecha de él
para ejecutar una aplicación. Dicha aplicación sólo tiene visibilidad sobre el sistema de ficheros
virtual del contenedor.

• Docker Compose
Es otro proyecto open source que permite definir aplicaciones multi-contenedor de una
manera sencilla. Es una alternativa más cómoda al uso del comando docker run, para trabajar con
aplicaciones con varios componentes.
Es una buena herramienta para gestionar entornos de desarrollo y de pruebas o para
processos de integración continua.

• Docker Machine
Es un proyecto open source para automatizar la creación de máquinas virtuales con Docker
instalado, en entornos Mac, Windows o Linux, pudiendo administrar así un gran número de
máquinas Docker.
Incluye drivers para Virtualbox, que es la opción aconsejada para instalaciones de Docker en
local, en vez de instalar Docker directamente en el host. Esto simplifica y facilita la creación o la
eliminación de una instalación de Docker, facilita la actualización de la versión de Docker o trabajar
con distintas instalaciones a la vez.
Usando el comando docker-machine podemos iniciar, inspeccionar, parar y reiniciar un
host administrado, actualizar el Docker client y el Docker daemon, y configurar un cliente para que
hable con el host anfitrión. A través de la consola de administración podemos administrar y correr
comandos Docker directamente desde el host. Éste comando docker-machine automáticamente
crea hosts, instala Docker Engine en ellos y configura los clientes Docker.