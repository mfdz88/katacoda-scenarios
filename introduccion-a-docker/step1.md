Las imágenes de Docker comienzan a partir de una imagen base. La imagen base debe incluir las dependencias de plataforma requeridas por su aplicación, por ejemplo,
frameworks o caracteristicas utiladas.

Esta imagen base se define como una instrucción en el Dockerfile. Las imágenes de Docker se crean basándose en el contenido de un Dockerfile. 
El Dockerfile es una lista de instrucciones que describen cómo implementar su aplicación.

En este ejemplo, nuestra imagen base es la versión Alpine de Nginx. Esto proporciona el servidor web configurado en la distribución de Linux Alpine.

<pre class="file" data-target="clipboard">
FROM nginx:alpine
COPY . /usr/share/nginx/html
</pre>
