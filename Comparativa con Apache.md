 <p align="center">
 <h1>Nginx VS  Apache</h1>
</p>
<div class="contenedor-imagenes">
  <img src="https://desarrolloweb.com/storage/tag_images/actual/nzShTvdaGzLCIO0FalGMkhnqXIcXcIwXABW9b4JU.png" "image" height="211" width="211">
  <img src="https://cdn.icon-icons.com/icons2/2107/PNG/512/file_type_nginx_icon_130305.png" alt= "image" height="211" width="211">
</div>


## Nginx y Apache son servidores web populares usados para enviar páginas web al navegador del usuario. En nuestro caso, desde un sitio de WordPress con un host. Datos rápidos:

##    Apache fue lanzado primero en 1995, luego llegó Nginx en el 2004.
##    Ambos son usados por grandes compañías Fortune 500 alrededor del mundo.
##    La posición de Nginx en el mercado ha ido en crecimiento constante en los últimos años.
##    En algunas ocasiones, Nginx ha tenido la ventaja competitiva en términos de desempeño.

<h1>APACHE<h1>


## Después del CERN httpd y el NCSA HTTPd de TimBerners-Lee durante los primeros años del internet, llegó Apache – lanzado originalmente en 1995 – y conquistó en unos instantes el mercado para convertirse en el servidor web más popular. Hoy en día, sigue ocupando una fuerte posición en el mercado, pero mayormente por razones de legado. Apache sigue siendo desarrollado y mantenido por el Apache Foundation, bajo la licencia Apache.

## Hay dos historias distintas sobre como Apache obtuvo su nombre. La primera versión dice que el nombre se originó de la famosa herencia Nativo Americana, mientras que la otra dice que el nombre es un chiste originado de la frase “a patchy server” o en español un servidor con muchos parches, después de recibir una gran cantidad de patches de software.
![pagina-base-ubuntu](https://user-images.githubusercontent.com/72433702/146513334-183848de-7a52-4910-a347-ba4077e04580.png)

## Un ejemplo del rol tan importante de Apache dentro del mundo de Linux es que sirve el nombre de su proceso de servidor es HTTPd, haciendo Apache sinónimo con el software de servidor web.

## Además de ser el primer jugador serio en el mercado de los servidores, parte de la proliferación de Apache es debida a su sistema de configuración y su archivo .htaccess.
## .htaccess

## Apache utiliza .htaccess para su configuración. Hay muchos tutoriales sobre cómo configurar, editar y trabajar con sus archivos ya que este provee mucha flexibilidad en la configuración de como Apache lidia con las peticiones entrantes. Algunos ejemplos son: distintas reglas de redirección, tamaños máximos de subida de archivos, reescrituras de URL, limites de memoria, protección de directorio (htpasswd), encabezados de expiración, encabezados de control-caché, encabezado de codificación, cookies, manipulaciones de query string.

## Por otro lado, Kinsta utiliza Nginx el cual no ofrece soporte para archivos .htaccess. Sin embargo, las opciones y reglas de sus archivos .htaccess pueden ser fácilmente “traducidas” a la regla reescrita de sintaxis de Nginx.

## Una de las principales “Ventajas” de Apache es que el servidor principal – el directorio principal del sitio web – cada nivel o directorio en el árbol de directorios pueden tener su propio archivo .htaccess con su propia configuración.

## Para proveedores de hosting compartido, esto es un sueño porque estos pueden ofrecer a cientos de usuarios en la misma maquina una forma de como configurar como sus sitios son servidos, sin que afecten a otros. Los clientes pueden configurar muchos de los detalles en un entorno restringido de hosting compartido, mientras que jamás tocarán la configuración del servidor global.

## Como dice la documentación oficial dice:

    «En general, usted debería usar los archivos .htaccess cuando uno no tenga acceso al archivo de configuración principal del servidor.»

## Esta flexibilidad, sin embargo, viene con un costo sobre el desempeño “¡permitiendo que los archivos .htaccess causen cambios en el desempeño, quiere o no usarlos!”

## Cada vez que los archivos .htaccess son habilitados, Apache tiene que atravesar todo el árbol del directorio desde un URL o archivo solicitado a través de todas las partes más altas hasta llegar al directorio raíz del servidor y luego cargarlas, por cada una de las peticiones. Esta necesita procesar estos archivos y reconfigurarse a sí mismo por cada uno de los directorios configurados de esta forma.

## Con los sitios de WordPress, las cosas se pueden poner realmente complejas. Un sitio típico de WordPress puede tener cientos de peticiones de distintos directorios.

## Desde los tipos de directorios /wp-content/uploads/yyyy/mm, típicamente tendrán múltiples peticiones en una sola carga de página, usualmente di directorios de distintos meses. Entonces habrá recursos estáticos del /wp-content/themes/parent-theme, /wp-content/themes/child-theme: estos incluirán javascript, archivos css, imágenes.

## Luego, también habrá /wp-content/plugins con archivos estáticos cargados usualmente de docenas de subdirectorios de plugin. Para cada uno de estos recursos, Apache tiene que atravesar todo árbol para encontrar la configuración.

## Un análisis ha demostrado que una configuración típica de WordPress, bastante común para sitios en hosts compartidos, incluirán 42 ejecuciones separadas .htaccess y 249 vistas separadas para el archivo .htaccess.

## Este es tan sólo un nivel de un servidor web. El visitante aún necesita esperar para que el proceso de PHP ejecute todo el stack de llamada de WordPress para crear un query de la base de datos y mandarlo a MySQL para armar la página web y enviarla al visitante.
Módulos

## Otra cosa que hizo popular a Apache es su sistema de módulo dinámico.

## Los Módulos – como una función que permite a los usuarios extender funcionalidad de servidor web – existen en Nginx y Apache. Apache permite que los usuarios instalen módulos una vez que el servidor web ya ha sido instalado y lanzado, y luego los habilita/deshabilita cuando sean necesarios. Las distribuciones basadas en Debian tienen comandos que permiten habilitar y deshabilitar estos módulos sin tener que editar los archivos de configuración: a2enmod y a2dismod.

## La lista oficial de módulos que vienen como parte de la distribución estándar de Apache están aquí y estas incluyen cosas como la compresión, encriptación, inicio de sesión, redirecciones a cosas más avanzadas como editar peticiones y respuestas con sintaxis avanzada.

 
 
 ## NGINX
 
 
## Nginx (también escrito como nginx o NGINX), entró en escena en el 2004, cuando fue lanzado por primera vez de forma pública por el desarrollador Ruso Igor Sysoev. Como Owen Garret, el jefe de proyecto de Nginx dijo:

    «Nginx fue escrito específicamente para resolver las limitantes de desempeño de los servidores web de Apache.»

## El servidor fue creado primero como una herramienta para escalar para el sitio web de rambler.ru en el 2002. Este viene en dos versiones: open source, con licencia tipo-BSD, y Nginx plus, con soporte y funciones empresariales adicionales.

## Después de ser lanzado, Nginx fue usado principalmente para servir archivos estáticos y como un balanceador de carga o proxy inverso en frente de instalaciones Apache. Mientras evolucionaba la red, y la necesidad de exprimir hasta la última gota de la velocidad y eficiencia de uso de hardware con este, más sitios empezaron a reemplazar Apache con Nginx por completo, gracias a un software mucho más maduro.
 
<p align="center">Configuración Nginx</p>

## Nginx no tiene un sistema de configuración como Apache, así que, a pesar de ser mucho más eficiente y rápido, no es tan usado con los proveedores de hosting. No resalta tanto en entornos compartidos como Apache.
