Las imágenes de Docker comienzan a partir de una imagen base. La imagen base debe incluir las dependencias de plataforma requeridas por su aplicación, por ejemplo,
frameworks o caracteristicas utiladas.

Esta imagen base se define como una instrucción en el Dockerfile. Las imágenes de Docker se crean basándose en el contenido de un Dockerfile. 
El Dockerfile es una lista de instrucciones que describen cómo implementar su aplicación.

En este ejemplo, nuestra imagen base es la versión Alpine de Nginx. Esto proporciona el servidor web configurado en la distribución de Linux Alpine.


<pre class="file" data-filename="Dockerfile.dockerfile" data-target="replace">
FROM nginx:alpine
COPY /Docker/index.html /usr/share/nginx/html
</pre>

<pre class="file" data-filename="index.html" data-target="replace">
 <h2>Hola mundo! - Marcelo</h2>
</pre>

`docker build -f Docker/Dockerfile.dockerfile -t  webserver-image:v1 .`{{execute}}

`docker images`{{execute}}