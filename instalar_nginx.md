# Instalar Servidor Web Nginx

[TOC]

Para instalar Nginx usar el gestor de paquetes apt:

```bash
jonay@ubuntu:~$ sudo apt-get install nginx curl
[sudo] password for jonay:
Leyendo lista de paquetes... Hecho
Creando árbol de dependencias
Leyendo la información de estado... Hecho
curl ya está en su versión más reciente (7.47.0-1ubuntu2.2).
Se instalarán los siguientes paquetes adicionales:
  fontconfig-config fonts-dejavu-core libfontconfig1 libgd3 libjbig0 libjpeg-turbo8 libjpeg8 libtiff5 libvpx3 libxpm4 libxslt1.1 nginx-common nginx-core
Paquetes sugeridos:
  libgd-tools fcgiwrap nginx-doc ssl-cert
Se instalarán los siguientes paquetes NUEVOS:
  fontconfig-config fonts-dejavu-core libfontconfig1 libgd3 libjbig0 libjpeg-turbo8 libjpeg8 libtiff5 libvpx3 libxpm4 libxslt1.1 nginx nginx-common nginx-core
0 actualizados, 14 nuevos se instalarán, 0 para eliminar y 45 no actualizados.
Se necesita descargar 2.999 kB de archivos.
Se utilizarán 9.781 kB de espacio de disco adicional después de esta operación.
¿Desea continuar? [S/n] S
Des:1 http://es.archive.ubuntu.com/ubuntu xenial/main amd64 libjpeg-turbo8 amd64 1.4.2-0ubuntu3 [111 kB]
Des:2 http://es.archive.ubuntu.com/ubuntu xenial/main amd64 libjbig0 amd64 2.1-3.1 [26,6 kB]
Des:3 http://es.archive.ubuntu.com/ubuntu xenial/main amd64 fonts-dejavu-core all 2.35-1 [1.039 kB]
Des:4 http://es.archive.ubuntu.com/ubuntu xenial-updates/main amd64 fontconfig-config all 2.11.94-0ubuntu1.1 [49,9 kB]
Des:5 http://es.archive.ubuntu.com/ubuntu xenial-updates/main amd64 libfontconfig1 amd64 2.11.94-0ubuntu1.1 [131 kB]
Des:6 http://es.archive.ubuntu.com/ubuntu xenial/main amd64 libjpeg8 amd64 8c-2ubuntu8 [2.194 B]
Des:7 http://es.archive.ubuntu.com/ubuntu xenial-updates/main amd64 libtiff5 amd64 4.0.6-1ubuntu0.1 [146 kB]
Des:8 http://es.archive.ubuntu.com/ubuntu xenial/main amd64 libvpx3 amd64 1.5.0-2ubuntu1 [732 kB]
Des:9 http://es.archive.ubuntu.com/ubuntu xenial-updates/main amd64 libxpm4 amd64 1:3.5.11-1ubuntu0.16.04.1 [33,8 kB]
Des:10 http://es.archive.ubuntu.com/ubuntu xenial-updates/main amd64 libgd3 amd64 2.1.1-4ubuntu0.16.04.6 [126 kB]
Des:11 http://es.archive.ubuntu.com/ubuntu xenial/main amd64 libxslt1.1 amd64 1.1.28-2.1 [145 kB]
Des:12 http://es.archive.ubuntu.com/ubuntu xenial-updates/main amd64 nginx-common all 1.10.0-0ubuntu0.16.04.4 [26,6 kB]
Des:13 http://es.archive.ubuntu.com/ubuntu xenial-updates/main amd64 nginx-core amd64 1.10.0-0ubuntu0.16.04.4 [428 kB]
Des:14 http://es.archive.ubuntu.com/ubuntu xenial-updates/main amd64 nginx all 1.10.0-0ubuntu0.16.04.4 [3.498 B]
Descargados 2.999 kB en 3s (804 kB/s)
Preconfigurando paquetes ...
Seleccionando el paquete libjpeg-turbo8:amd64 previamente no seleccionado.
(Leyendo la base de datos ... 59910 ficheros o directorios instalados actualmente.)
Preparando para desempaquetar .../libjpeg-turbo8_1.4.2-0ubuntu3_amd64.deb ...
Desempaquetando libjpeg-turbo8:amd64 (1.4.2-0ubuntu3) ...
Seleccionando el paquete libjbig0:amd64 previamente no seleccionado.
Preparando para desempaquetar .../libjbig0_2.1-3.1_amd64.deb ...
Desempaquetando libjbig0:amd64 (2.1-3.1) ...
Seleccionando el paquete fonts-dejavu-core previamente no seleccionado.
Preparando para desempaquetar .../fonts-dejavu-core_2.35-1_all.deb ...
Desempaquetando fonts-dejavu-core (2.35-1) ...
Seleccionando el paquete fontconfig-config previamente no seleccionado.
Preparando para desempaquetar .../fontconfig-config_2.11.94-0ubuntu1.1_all.deb ...
Desempaquetando fontconfig-config (2.11.94-0ubuntu1.1) ...
Seleccionando el paquete libfontconfig1:amd64 previamente no seleccionado.
Preparando para desempaquetar .../libfontconfig1_2.11.94-0ubuntu1.1_amd64.deb ...
Desempaquetando libfontconfig1:amd64 (2.11.94-0ubuntu1.1) ...
Seleccionando el paquete libjpeg8:amd64 previamente no seleccionado.
Preparando para desempaquetar .../libjpeg8_8c-2ubuntu8_amd64.deb ...
Desempaquetando libjpeg8:amd64 (8c-2ubuntu8) ...
Seleccionando el paquete libtiff5:amd64 previamente no seleccionado.
Preparando para desempaquetar .../libtiff5_4.0.6-1ubuntu0.1_amd64.deb ...
Desempaquetando libtiff5:amd64 (4.0.6-1ubuntu0.1) ...
Seleccionando el paquete libvpx3:amd64 previamente no seleccionado.
Preparando para desempaquetar .../libvpx3_1.5.0-2ubuntu1_amd64.deb ...
Desempaquetando libvpx3:amd64 (1.5.0-2ubuntu1) ...
Seleccionando el paquete libxpm4:amd64 previamente no seleccionado.
Preparando para desempaquetar .../libxpm4_1%3a3.5.11-1ubuntu0.16.04.1_amd64.deb ...
Desempaquetando libxpm4:amd64 (1:3.5.11-1ubuntu0.16.04.1) ...
Seleccionando el paquete libgd3:amd64 previamente no seleccionado.
Preparando para desempaquetar .../libgd3_2.1.1-4ubuntu0.16.04.6_amd64.deb ...
Desempaquetando libgd3:amd64 (2.1.1-4ubuntu0.16.04.6) ...
Seleccionando el paquete libxslt1.1:amd64 previamente no seleccionado.
Preparando para desempaquetar .../libxslt1.1_1.1.28-2.1_amd64.deb ...
Desempaquetando libxslt1.1:amd64 (1.1.28-2.1) ...
Seleccionando el paquete nginx-common previamente no seleccionado.
Preparando para desempaquetar .../nginx-common_1.10.0-0ubuntu0.16.04.4_all.deb ...
Desempaquetando nginx-common (1.10.0-0ubuntu0.16.04.4) ...
Seleccionando el paquete nginx-core previamente no seleccionado.
Preparando para desempaquetar .../nginx-core_1.10.0-0ubuntu0.16.04.4_amd64.deb ...
Desempaquetando nginx-core (1.10.0-0ubuntu0.16.04.4) ...
Seleccionando el paquete nginx previamente no seleccionado.
Preparando para desempaquetar .../nginx_1.10.0-0ubuntu0.16.04.4_all.deb ...
Desempaquetando nginx (1.10.0-0ubuntu0.16.04.4) ...
Procesando disparadores para libc-bin (2.23-0ubuntu5) ...
Procesando disparadores para man-db (2.7.5-1) ...
Procesando disparadores para ufw (0.35-0ubuntu2) ...
Procesando disparadores para ureadahead (0.100.0-19) ...
Procesando disparadores para systemd (229-4ubuntu16) ...
Configurando libjpeg-turbo8:amd64 (1.4.2-0ubuntu3) ...
Configurando libjbig0:amd64 (2.1-3.1) ...
Configurando fonts-dejavu-core (2.35-1) ...
Configurando fontconfig-config (2.11.94-0ubuntu1.1) ...
Configurando libfontconfig1:amd64 (2.11.94-0ubuntu1.1) ...
Configurando libjpeg8:amd64 (8c-2ubuntu8) ...
Configurando libtiff5:amd64 (4.0.6-1ubuntu0.1) ...
Configurando libvpx3:amd64 (1.5.0-2ubuntu1) ...
Configurando libxpm4:amd64 (1:3.5.11-1ubuntu0.16.04.1) ...
Configurando libgd3:amd64 (2.1.1-4ubuntu0.16.04.6) ...
Configurando libxslt1.1:amd64 (1.1.28-2.1) ...
Configurando nginx-common (1.10.0-0ubuntu0.16.04.4) ...
Configurando nginx-core (1.10.0-0ubuntu0.16.04.4) ...
Configurando nginx (1.10.0-0ubuntu0.16.04.4) ...
Procesando disparadores para libc-bin (2.23-0ubuntu5) ...
Procesando disparadores para systemd (229-4ubuntu16) ...
Procesando disparadores para ureadahead (0.100.0-19) ...
Procesando disparadores para ufw (0.35-0ubuntu2) ...
```

Configurar Nginx para que use la codificación _UTF-8_ por defecto, para ello, editar el fichero _/etc/nginx/nginx.conf_ y añadir la siguiente línea a la directiva http:

```bash
...
http {
        charset UTF-8;
        ...
}
```

Para editar el fichero _/etc/nginx/nginx.conf_, al no contar con entorno gráfico, hacer uso del editor de texto nano para abrir el fichero de configuración:

```bash
jonay@ubuntu:~$ sudo nano /etc/nginx/nginx.conf
```

Una vez añadida la línea, pulsar CTRL+o para guardar los cambios y CTRL+x para salir del fichero de configuración. El fichero de configuración debería quedar de la siguiente manera:

```bash
jonay@ubuntu:~$ cat /etc/nginx/nginx.conf
user www-data;
worker_processes auto;
pid /run/nginx.pid;

events {
        worker_connections 768;
        # multi_accept on;
}

http {
        charset UTF-8;
        ##
        # Basic Settings
        ##

        sendfile on;
        tcp_nopush on;
        tcp_nodelay on;
        keepalive_timeout 65;
        types_hash_max_size 2048;
        # server_tokens off;

        # server_names_hash_bucket_size 64;
        # server_name_in_redirect off;

        include /etc/nginx/mime.types;
        default_type application/octet-stream;

        ##
        # SSL Settings
        ##

        ssl_protocols TLSv1 TLSv1.1 TLSv1.2; # Dropping SSLv3, ref: POODLE
        ssl_prefer_server_ciphers on;

        ##
        # Logging Settings
        ##

        access_log /var/log/nginx/access.log;
        error_log /var/log/nginx/error.log;

        ##
        # Gzip Settings
        ##

        gzip on;
        gzip_disable "msie6";

        # gzip_vary on;
        # gzip_proxied any;
        # gzip_comp_level 6;
        # gzip_buffers 16 8k;
        # gzip_http_version 1.1;
        # gzip_types text/plain text/css application/json application/javascript text/xml application/xml application/xml+rss text/javascript;

        ##
        # Virtual Host Configs
        ##

        include /etc/nginx/conf.d/*.conf;
        include /etc/nginx/sites-enabled/*;
}


#mail {
#       # See sample authentication script at:
#       # http://wiki.nginx.org/ImapAuthenticateWithApachePhpScript
#
#       # auth_http localhost/auth.php;
#       # pop3_capabilities "TOP" "USER";
#       # imap_capabilities "IMAP4rev1" "UIDPLUS";
#
#       server {
#               listen     localhost:110;
#               protocol   pop3;
#               proxy      on;
#       }
#
#       server {
#               listen     localhost:143;
#               protocol   imap;
#               proxy      on;
#       }
#}
```

Recargar la configuración de Nginx:

```bash
jonay@ubuntu:~$ sudo systemctl reload nginx
```

Usar la librería curl para comprobar la configuración del servidor y ver que los cambios se han realizado correctamente:

```bash
jonay@ubuntu:~$ curl -I http://localhost
HTTP/1.1 200 OK
Server: nginx/1.10.0 (Ubuntu)
Date: Tue, 11 Apr 2017 10:46:20 GMT
Content-Type: text/html; charset=UTF-8
Content-Length: 612
Last-Modified: Tue, 11 Apr 2017 10:39:25 GMT
Connection: keep-alive
ETag: "58ecb25d-264"
Accept-Ranges: bytes
```

Debería aparecer la línea _Content-Type: text/html; charset=UTF-8_ en la salida del comando _curl_.


## Configurar la Máquina Virtual para poder acceder al servidor web desde nuestro equipo.

Se pretende poder acceder al servidor web desde fuera de la Máquina Virtual, es decir, desde el equipo donde hemos instalado el VirtualBox.

Abrir la configuración de la Máquina Virtual:

<kbd>![img01](/images/01_open_nginx_port/img01.png)</kbd>

En la configuración de red, abrir el _Reenvío de puertos_:

<kbd>![img02](/images/01_open_nginx_port/img02.png)</kbd>

Crear una nueva regla con los siguientes valores y pulsamos _Ok_ hasta salir de la configuración:
* **Puerto Anfitrión**: 8080
* **Puerto Invitado**: 80

<kbd>![img03](/images/01_open_nginx_port/img03.png)</kbd>

Para acceder al servidor Nginx, abrir en nuestro equipo (equipo donde tenemos instalado el VirtualBox) un navegador web y acceder a la URL _http://localhost:8080_:

<kbd>![img04](/images/01_open_nginx_port/img04.png)</kbd>

## Subir contenido al servidor Nginx

Para subir un fichero HTML a nuestro servidor Nginx, es necesario usar un cliente FTP. Para este tutorial se ha usado FileZilla Client, pero se pueden usar otros clientes Web como WinSCP, ...

Por defecto, en nuestra Máquina Virtual, el usuario root es el propietario de la carpeta _/var/www/html_, que es la ruta por defecto donde el servidor NGinx va a buscar las páginas web, por lo que sólo el usuario root puede escribir en esa carpeta.

Así que lo primero que hay que hacer es darle permisos de escritura al usuario creado durante el proceso de instalación de Ubuntu 16.04 Server para que puda subir fichero a la carpeta _/var/www/html_ en este caso:

```bash
# Comprobamos los permisos de la carpeta /var/www/html:
jonay@ubuntu:/var/www$ ls -l
total 4
drwxr-xr-x  2 root root 4096 abr 11 11:39 html

# Cambiamos el grupo propietario de la carpeta de root a www-data
jonay@ubuntu:/var/www$ sudo chown -R :www-data /var/www/html
[sudo] password for jonay:

# Dar permisos de escritura al grupo www-data:
jonay@ubuntu:/var/www$ sudo chmod -R g+w /var/www/html

# Comprobamos los permisos actuales de la carpeta /var/www/html:
jonay@ubuntu:/var/www$ ls -l /var/www/
total 4
drwxrwxr-x 2 root www-data 4096 abr 11 11:39 html

# Configurar el usuario de la instalación de Ubuntu 16.04 Server, en este caso jonay, para que forme parte del grupo www-data:
jonay@ubuntu:/var/www$ sudo usermod -a -G www-data jonay

# Comprobamos los grupos a los que pertenece el usuario de instalación de Ubuntu 16.04 Server, en este caso jonay, en el listado debe estar el grupo www-data:
jonay@ubuntu:/var/www$ groups jonay
jonay : jonay adm cdrom sudo dip www-data plugdev lxd lpadmin sambashare
```

Con esto el usuario de la instalación de Ubuntu 16.04 Server, en este caso jonay, ya tiene permisos de escritura sobre la carpeta:

Crear en nuestro equipo una página web HTML5 y guardarla con el nombre _index.html_:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="utf-8" />
    <title>Página de pruebas</title>
  </head>
  <body>
    <h1>Mi Primer Título</h1>
    <p>Mi primer párrafo.</p>
  </body>
</html> 
```

Instalar el cliente FileZilla, se puede descargar de la siguiente dirección:

* [https://download.filezilla-project.org/client/FileZilla_3.25.1_win64-setup_bundled.exe](https://download.filezilla-project.org/client/FileZilla_3.25.1_win64-setup_bundled.exe)

Abrir el cliente FileZilla y pulsar en el _Gestor de Sitios_:

<kbd>![img01](/images/02_upload_nginx_content/img01.png)</kbd>

Configurar un _Nuevo sitio_ con los siguientes datos:

* **Nombre del sitio**: localhost
* **Servidor**: localhost
* **Puerto**: 2222
* **Protocolo**: SFTP - SSH File Transfer Protocol
* **Modo de acceso**: Preguntar la contraseña
* **Usuario**: Usuario creado durante el proceso de instalación de Ubuntu 16.04 Server

Una vez añadidos los datos, pulsar en _Aceptar_:

<kbd>![img02](/images/02_upload_nginx_content/img02.png)</kbd>

<kbd>![img03](/images/02_upload_nginx_content/img03.png)</kbd>

Ahora volver a pulsar sobre el _Gestor de Sitios_ y seleccionar el sitio que seleccionamos anteriormente:

<kbd>![img04](/images/02_upload_nginx_content/img04.png)</kbd>

Nos pide el password del usuario de instalación, en este caso, el password del usuario _jonay_. Marcar la opción _Remember password until FileZilla is closed_ y pulsar _Aceptar_:

<kbd>![img05](/images/02_upload_nginx_content/img05.png)</kbd>

El siguiente mensaje aparece porque es la primera vez que accedemos a la Máquina Virtual con el cliente Filezilla, marcamos la opción _Confiar siempre en este sitio, añadir su clave a la caché_ y pulsar _Aceptar_:

<kbd>![img06](/images/02_upload_nginx_content/img06.png)</kbd>

En el panel de la izquierda, en _Sitio local_, seleccionar la carpeta donde hemos guardado nuestra página web _index.html_ creada anteriormente, en este caso, la carpeta _D:\Repositorio\html5_. En el panel de la derecha, en _Sitio remoto_, seleccionar la carpeta donde va a estar ubicada la página web en el servidor Nginx, en este caso _/var/www/html_:

<kbd>![img07](/images/02_upload_nginx_content/img07.png)</kbd>

Arrastrar el fichero _index.html_ del panel de la izquierda al panel de la derecha, ahora debe aparecer el fichero _index.html_en el panel de la derecha:

<kbd>![img08](/images/02_upload_nginx_content/img08.png)</kbd>

Con esto acabamos de transferir el fichero _index.html_ desde nuestro equipo, a la carpeta _/var/www/html_ de la Máquina Virtual.

Abrir un navegador web y escribir la URL _http://localhost:8080_, si todo ha ido bien debería cargar nuestra página web _index.html_:

<kbd>![img09](/images/02_upload_nginx_content/img09.png)</kbd>

No hace falta añadir el nombre del archivo _index.html_ a la dirección web, los servidores web, si no se le indica el nombre de la página web, busca por defecto el fichero _index.html_.
