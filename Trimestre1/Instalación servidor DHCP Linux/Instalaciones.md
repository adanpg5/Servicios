# **Instalaciones del servidor DHCP en Linux**

<hr>

# Creamos las máquinas.

* Tenemos que crear dos máquinas, una cliente y otra servidor.
  * La servidor le ponemos adaptador puente (temporalmente).
  * La cliente le ponemos red interna llamada "interna".

<hr>

# Proceso.

* Encendemos la máquina **servidor** e instalamos el servidor DHCP utilizando el comando `sudo apt-get install isc-dhcp-server`.


![imagen](./img/c1.PNG)

* Vamos al archivo de configuración del servidor *dhcp*, la ruta es `/etc/dhcp/dhcpd.config`
  * Comentamos todas las líneas que aún no estén comentadas, y haremos nuestra propia configuración.
  * Creamos un rango de cesión primero, de manera que cogemos la *subnet que vamos a utlizar, su máscara, el gateway por defecto, los servidores DNS y el rango de IPs*.
  * Acto seguido creamos una reserva de dirección para la máquina cliente, con lo que pondremos su dirección **MAC** y la IP que tendrá.


![imagen](./img/c3.PNG)

* Ahora reiniciamos el servidor DHCP.
  * Primero utilizamos `sudo service isc-dhcp-server-stop`
  * Y luego igual, pero en vez de `stop`, con un `start`.
  * Para comprobar que funciona, `sudo service isc-dhcp-server-status`.

![imagen](./img/c4.PNG)

<hr>

# Comprobación.

* Por último vamos a la máquina **cliente**, y esperamos un poco, o bien, reiniciamos.
  * Hacemos un `sudo ifconfig` para comprobar nuestra IP, y podemos ver que tenemos la IP ofrecida por el servidor DHCP.

![imagen](./img/c5.PNG)

<hr>
