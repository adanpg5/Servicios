# IIS Windows 2012 Server IV

* Crea una nueva zona de búsqueda directa en los servicios DNS asociado al dominio miEmpresa. Crea también una carpeta miEmpresa en C:\ y una subcarpeta ‘principal’.

![img](./img/000097.png)

![img](./img/000098.png)

* Crea  un  nuevo  sitio  web  denominado miEmpresa en  IIS  asociado  a  la  subcarpeta  anterior  y  con  acceso a través de la dirección www.miEmpresa.com. Actualiza DNS adecuadamente

![img](./img/000099.png)

* Configuración  A:  Siguiendo  los  pasos  del  tutorial  correspondiente,  configura  el  nuevo  sitio  para que se pueda acceder (sólo) como sitio web seguro (https) con un Certificado Autofirmado

![img](./img/000100.png)

![img](./img/000101.png)

![img](./img/000102.png)

* Configuración B:
 Crearemos un nuevo sitio seguro (tienda.miempresa.com) con la generación de
un  Certificado  Digital
a  través  de  la  aplicación  OpenSSL.  Para  empezar,  realizaremos  la  solicitud  de un nuevo certificado de servidor para nuestro sitio seguro (crear fichero certreq.txt).
  * Descargar e instalar OpenSSL para Windows.

![img](./img/000103.png)

* A través de OpenSSl genera un nuevo certificad
o de servidor, siguiendo los pasos que se detallan
en tutorial web (y comprobando los ficheros generados en cada paso): generar una clave privada
de  la  entidad  certificadora,  crear  un  certificado  digital  de  la  entidad  certificadora  y,  finalmente,  
crear un certificado digital de nuestra web.

![img](./img/000104.png)

![img](./img/000105.png)

![img](./img/000106.png)

![img](./img/000107.png)

![img](./img/000108.png)

* Importar  el  nuevo  certificado  de  servidor  creado  para  completar  la  petición  pendiente  en nuestro sitio seguro ‘pagos’.

![img](./img/000109.png)

* Requerir  que  nuestros  sitio  seguros  sólo  se  pueda  acceder  mediante  una  conexión  segura  y reiniciar los sitios web.

![img](./img/000110.png)

* Finalmente, acceder mediante http y mediante https a los sitios seguros desde el propio servidor y
desde un cliente W7, aceptando los posibles problemas con la entidad certificadora.

![img](./img/000113.png)

---

# IIS Windows 2012 Server IV B

* Necesitamos  crear  una  carpeta  empleados  (dentro  de  miEmpresa)  y, dentro de esta, tres o cuatro subcarpetas personales con nombres de empleados y una, denominada común, a la que
tendrán acceso todos los empleados, pero no otros usuarios sin identificar.

![img](./img/000114.png)

* Crearemos  el  nuevo  sitio  web,  como  subdominio  de  nuestro  dominio  principal,  asociado a la carpeta genérica empleados.

![img](./img/000115.png)

![img](./img/000116.png)

* Colocar un fichero index.html diferente en cada una de las carpetas creadas, con el objetivo de
poder comprobar el acceso desde un navegador.

![img](./img/000117.png)

* Para el sitio web creado y para cada una de sus carpetas, deshabilitamos el acceso anónimo.
  * Para el sitio web creado y para cada una de sus carpetas, deshabilitamos el acceso anónimo.
Agregar función de Autenticación Básica a nuestro Servicio de IIS a través de la Administración del Servidor.

![img](./img/000118.png)

![img](./img/000119.png)

![img](./img/000120.png)

* En   Active   Directory, crearemos un usuario   para   cada empleado (tantos como carpetas personales) y un grupo Empleados que los incluya a todos.

![img](./img/000121.png)

![img](./img/000122.png)

![img](./img/000123.png)

![img](./img/000124.png)

![img](./img/000125.png)

![img](./img/000127.png)

* Desactivamos,  para  la  carpeta  empleados,  los  permisos  heredables  a  través  de  las  opciones  avanzadas  en  la  ficha  de  seguridad.  Añadimos  grupo  de  Administradores  con  Control  Total y grupo Empleados con Lectura y Ejecución+ Mostrar Carpeta+Leer.
  * Realizamos   el   mismo   procedimiento   para   cada   una   de   las   carpetas   personales   de   los   empleados, colocando como usuarios autorizados el Grupo de Administradores (Control Total)
y el empleado propietario de cada carpeta (con los permisos que creas convenientes).
    * Realizamos   el   mismo   procedimiento   para   la   carpeta   ‘comun’,   colocando   como   usuarios   autorizados  el  Grupo  de  Administradores  (Control  Total)  y  el  grupo  Empleados  (con  los  
permisos que creas convenientes).

![img](./img/000129.png)

![img](./img/000130.png)

![img](./img/000131.png)

![img](./img/000132.png)

* Comprobamos  el  acceso,  tanto  desde  el  servidor  como  desde el  cliente  W7, a las diferentes carpetas con distintos usuarios.

![img](./img/000133.png)

![img](./img/000134.png)

![img](./img/000135.png)

![img](./img/000136.png)

![img](./img/000137.png)

![img](./img/000138.png)

---
