Akguno de los comandos utiles y mas utilizados en docker son los siguientes: 

<b>WORKDIR</b>
Permite especificar en qué directorio se va a ejecutar una instrucción RUN, CMD o ENTRYPOINT.

<b>EXPOSE</b>
Se utiliza para asociar puertos, permitiéndonos exponer un contenedor al exterior (internet,
host,etc.). Esta instrucción le especifica a Docker que el contenedor escucha en los puertos
especificados. Pero EXPOSE no hace que los puertos puedan ser accedidos desde el host, para esto
debemos mapear los puertos usando la opción -p en docker run.
Por ejemplo:
EXPOSE 80 443
docker run centos:centos7 -p 8080:80
53

<b>ENTRYPOINT</b>
Cualquier argumento que pasemos en la línea de comandos mediante docker run serán
anexados después de todos los elementos especificados mediante la isntrucción ENTRYPOINT, y
anulará cualquier elemento especificado con CMD. Esto permite pasar cualquier argumento al
punto de entrada.
Sintaxis:
ENTRYPOINT [“ejecutable”,”parámetro1”,”parámetro2”] → forma de ejecución
ENTRYPOINT comando parámetro1 parámetro 2 → forma shell
ENTRYPOINT nos permite indicar qué comando se va a ejecutar al iniciar el contenedor,
pero en este caso el usuario no puede indicar otro comando al iniciar el contenedor. Si usamos esta
opción es porque no esperamos que el usuario ejecute otro comando que el especificado