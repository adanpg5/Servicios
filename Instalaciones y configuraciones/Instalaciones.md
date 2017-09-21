# **Instalaciones y configuraciones**
<hr>
# 1. Creamos las máquinas

Y procedemos a instalar sus respectivos sistemas operativos.

 ![imagen](./images/Ubuntu/c0.PNG)

 >Windows 10 Cliente = 2048 RAM, 32GB Dinámicos, Adaptador puente

 >Windows Server 2012 = 4096 RAM, 32GB Dinámicos, Adaptador puente

>UbuntuCliente = 1024 RAM, 15GB Dinámicos, Adaptador puente

>UbuntuServer = 2048 RAM, 15GB Dinámicos, Adaptador puente

<hr>
# 2. Ubuntu

- Insertamos una ISO de **Ubuntu** en la máquina de *Cliente* y en la de *Servidor*, iniciamos y a continuación empezamos a instalar.


![imagen](./images/Ubuntu/c1.PNG)

![imagen](./images/Ubuntu/c2.PNG)

![imagen](./images/Ubuntu/c3.PNG)

![imagen](./images/Ubuntu/c4.PNG)

![imagen](./images/Ubuntu/c5.PNG)

![imagen](./images/Ubuntu/c6.PNG)

- Y por último cambiamos la IP de la máquina servidor, editando así una IP dentro del rango disponible

![imagen](./images/Ubuntu/c7.PNG)

<hr>

# 3. Windows

- Al igual que en *Ubuntu*, tenemos que insertar las ISOS de **Windows** en dichas máquinas y hacemos la instalación.

![imagen](./images/Windows/c1.PNG)

- Instalamos el ***Active Directory*** en el servidor.

![imagen](./images/Windows/c2.PNG)

![imagen](./images/Windows/c3.PNG)

![imagen](./images/Windows/c4.PNG)

![imagen](./images/Windows/c5.PNG)

- Antes de seguir con la instalación de ***Active Directory*** configuramos la IP de dicha máquina, dentro de un determinado rango.


![imagen](./images/Windows/c6.PNG)

![imagen](./images/Windows/c7.PNG)

- Seleccionamos Servicios de dominio de Active Directory, que es lo que nos interesa.


![imagen](./images/Windows/c8.PNG)

![imagen](./images/Windows/c9.PNG)

- Y creamos por último el dominio en el que entraremos con el cliente.


![imagen](./images/Windows/c10.PNG)

![imagen](./images/Windows/c11.PNG)

![imagen](./images/Windows/c12.PNG)

<hr>

- Ahora en el ***CLIENTE*** tenemos que cambiar nuestra IP, dejando la dirección automáticamente por el servidor, y asignando en direcciones DNS como preferido la IP de la máquina **servidor**, y como secundaria, por ejemplo, la de google.

![imagen](./images/Windows/c13.PNG)

>Después de esta acción, vamos a Equipo>Propiedades>Cambiar y ponemos el nombre del dominio que creamos en el servidor, en mi caso es adan.asir, y te pedirá un *Usuario* y *contraseña*, que ahí lo rellenaremos con los datos de nuestro usuario administrador del **servidor**.

![imagen](./images/Windows/c14.PNG)
