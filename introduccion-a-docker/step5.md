
Un contenedor segun la documentacion oficial de docker es : "Es una pieza de software liviana, independiente, empaquetable 
y ejecutable que incluye todo lo que necesita para corrercódigo, runtime, herramientas de sistema, librerías y 
configuraciones"(Documentacion Ofidiclal de docker, 2021)

En otras palabras, un contenedor es una pieza de software que puede ejecutarse sin necesidad de nada adicional.

docker run [OPTIONS] IMAGE [COMMAND] [ARG....]
Entre las opciones se encuentran (lista completa aquí):
-a, --attach: para conectarnos a un contenedor que está corriendo.
-d, --detach: corre un contenedor en segundo plano.
-i, --interactive: habilita el modo interactivo.
--name: le pone nombre a un contenedor.

<h4>Creacion del contendor</h4>

Como vimos anteriormente un contenedor es la instancias de una imagen, para crear un contendor apartir de una imagen:

`docker run -d -p 80:80 webserver-image:v1`{{execute}}

Consultar contenedores diponibles: 
`docker ps`{{execute}}