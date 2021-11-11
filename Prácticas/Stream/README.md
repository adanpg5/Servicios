# Servicio streaming. Práctica 1.

* Descargar e instalar IIS Media Services, soporte de Streaming para el Servidor web IIS.
Comprobar que aparecen, tanto a nivel de servidor como en los sitios web, las nuevas
opciones de Servicios Multimedia.

![img](./img/captura1.PNG)

![img](./img/captura2.PNG)

![img](./img/captura3.PNG)

![img](./img/captura4.PNG)

* Descargar   ejemplos   de   emisiones   multimedia   codificadas   para   su   emisión   en
streaming Windows Media Samples. Descomprimir sus contenidos en dos carpetas
independientes que nos servirán para su publicación en streaming.

![img](./img/captura6.PNG)

![img](./img/captura7.PNG)

![img](./img/captura8.PNG)

* Crear   dos   nuevos   sitios   web   asociados   a   los   contenidos   multimedia   descargados:
bunny.tudominio.ext y elephants.tudominio.ext. Crear previamente los registros DNS
asociados. Los sitios web deben ofrecerse a través de los enlaces descritos y apuntar
a las carpetas físicas donde alojamos los contenidos multimedia respectivos.

![img](./img/captura5.PNG)

![img](./img/captura9.PNG)

![img](./img/captura10.PNG)

![img](./img/captura11.PNG)

![img](./img/captura12.PNG)

* Descargar y descomprimir el cliente de reproducción SmoothMediaPlayer. Copiar los
ficheros extraidos en las carpetas de los sitios web – streaming y editar el fichero
SmoothStreamingPlayer.html   para   adaptarlo   a   la   emisión   en   streaming   de   los
contenidos de cada sitio.

![img](./img/captura13.PNG)

![img](./img/captura14.PNG)

![img](./img/captura15.PNG)

![img](./img/captura16.PNG)

![img](./img/captura17.PNG)

![img](./img/captura18.PNG)

![img](./img/captura19.PNG)

* Configurar ambos sitios web  para que accedan de forma predeterminada al archivo
html anterior.

![img](./img/captura20.PNG)

![img](./img/captura21.PNG)

* Comprobar desde un navegador en el servidor la reproducción de ambos sitios.

![img](./img/captura22.PNG)

![img](./img/captura23.PNG)

![img](./img/captura24.PNG)

* Comprobar desde un navegador en una máquina cliente la reproducción de ambos
sitios.

![img](./img/captura25.PNG)

![img](./img/captura26.PNG)

* En las características de los Servicios Multimedia de uno de los sitios, examinar la
Limitación   de   Velocidad   de   Bits.   Incluir   un   comentario   sobre   su   significado   en   el
informe.

![img](./img/captura27.PNG)

* Examinar también la característica de Presentaciones de Transmisión por Secuencia
Suave (Smooth Streaming) para comprobar el punto de acceso a la presentación y sus
contenidos (pistas de audio / video).

![img](./img/captura28.PNG)

# Servidor streaming. Práctica 2.

* Descargar e instalar Microsoft Expression Encoder, para su correcta ejecución debes instalar
la Característica de Experiencia de Escritorio en tu servidor Windows 2012.

![img](./img/captura29.PNG)

![img](./img/captura30.PNG)

![img](./img/captura33.PNG)

* Vamos a crear un nuevo sitio web en IIS para la emisión de una presentación multimedia en
Streaming pero, en este caso, se van a utilizar contenidos propios. Asi que, en primer lugar
debes contar con una serie de archivos de audio y/o video (formatos mp3, wma, avi, etc.).
  * A continuación creamos el sitios IIS (lo podemos llamar Playlist) que estaría asociado a un
registro DNS (playlist.tudominio.ext) y a una carpeta física (por ahora vacía) en cualquier
lugar de tu disco duro.

![img](./img/captura31.PNG)

![img](./img/captura32.PNG)

* En este momento, vamos a realizar la codificación de los archivos multimedia que hemos
elegido para que puedan emitirse en streaming (ten en cuenta que no se aceptan todos los
formatos). Para ello utilizaremos la aplicación Mircosoft Expression Encoder.

![img](./img/captura34.PNG)

* Al Ejecutar el codificador (Encoder) seleccionaremos la opción Proyecto de Silverlight. Luego
añadiremos   los   archivos   que   nos   interesen   y   procederemos   a   codificarlos.   Antes
ajustaremos el directorio de salida de la codificación a la carpeta donde alojamos el sitio
web Playlist.
  * Ahora estableceremos como archivo predeterminado la página html que se ha creado en la
carpeta Playlist como punto de acceso a la presentación en streaming y reiniciaremos el sitio
web.

![img](./img/captura35.PNG)

![img](./img/captura36.PNG)

* Sólo nos queda comprobar en el servidor y en un cliente la correcta reproducción de
nuestro Playlist.

![img](./img/captura37.PNG)

![img](./img/captura38.PNG)
