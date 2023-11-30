# Odoo_Commands

```
sudo apt-get update
```
```
sudo apt-get upgrade
```
```
sudo useradd -m -d /opt/odoo -U -r -s /bin/bash odoo
```
```
sudo passwd odoo
```
```
sudo adduser odoo sudo
```
```
su odoo
```
```
cd ~
```
```
git clone https://github.com/odoo/odoo.git --depth 1 --branch 16.0 --single-branch
```
```
sudo apt-get install python3-pip
```
```
python3 --version
```
```
pip3 --version
```
```
sudo apt-get install postgresql postgresql-client
```
```
sudo passwd postgres
```
```
su postgres
```
```
psql
```
```
CREATE ROLE odoo WITH LOGIN PASSWORD 'odoo';
```
```
CREATE DATABASE odoo;
```
```
ALTER DATABASE odoo OWNER TO odoo;
```
```
ALTER USER odoo WITH CREATEDB;
```
```
\q
```
```
su - odoo
```
```
psql
```
```
\c odoo
```
```
\q
```
```
cd odoo
```
```
sudo -H pip3 install setuptools wheel
```
```
sudo apt-get install python3-cffi
```
```
sudo apt-get install python3-dev
```
```
sudo apt-get install build-essential
```
```
sudo apt-get install libldap2-dev
```
```
sudo apt-get install libsasl2-dev
```
```
sudo apt-get install libpq-dev
```
```
sudo -H pip3 install -r requirements.txt
```
```
python3 odoo-bin --addons-path=addons -d odoo -i odoo
```
------
# apt-get
Instalar un paquete:
```
# apt-get install <paquete>
```
Desinstalar un paquete:
```
# apt-get remove <paquete>
```
Eliminar un paquete incluidos sus ficheros de configuración:
```
# apt-get purge <paquete>
```
Eliminar de forma automática aquellos paquetes que no se estén utilizando:
```
# apt-get autoremove
```
Actualizar un paquete a la última versión disponible en el repositorio:
```
# apt-get update <paquete>
```
Actualizar el sistema. Actualizará todos los paquetes que dispongan de una versión superior
dentro de la rama instalada de la distribución:
```
# apt-get upgrade
```
Actualizar la distribución completa. Actualizará nuestro sistema a la siguiente versión disponible
de la distribución:
```
# apt-get dist-upgrade
```
Descargar únicamente las fuentes de un paquete para manipularlas de forma manual:
```
# apt-get source <paquete>
```
Limpiar cachés, paquetes descargados, etc:
```
# apt-get clean
# apt-get autoclean
```
Verificar que no tenemos ninguna dependencia incumplida:
```
# apt-get check
```
# apt-cache
Buscar un paquete en los repositorios, se puede especificar un patrón, expresión regular, el
nombre exacto del paquete, etc:
```
# apt-cache search <paquete>
```
Mostrar información sobre un paquete específico (nombre del paquete, versión,
dependencias…):
```
# apt-cache showpkg <paquete>
```
Mostrar información del paquete incluyendo la descripción, información del paquete como su
sitio web, página de bugs…
```
# apt-cache show <paquete>
```
Mostrar dependencias de un paquete:
```
# apt-cache depends <paquete>
```
Mostrar los nombres de todos los paquetes instalados en el sistema:
```
# apt-cache pkgnames
```
# aptitude
Es una interfaz para apt. Muestra una lista de paquetes de software y permite al
usuario elegir de modo interactivo cuáles desea instalar o eliminar. Dispone de un poderoso
sistema de búsqueda que utiliza patrones de búsqueda flexibles, que facilitan al usuario
entender las complejas relaciones de dependencia que puedan existir entre los paquetes. En
un principio, se diseñó para distribuciones GNU/Linux Debian, pero hoy día también se puede
utilizar en distribuciones basadas en paquetes RPM.
Instalar paquetes:
```
# sudo aptitude install <paquetes>
```
Desinstalar paquetes:
```
# sudo aptitude remove <paquetes>
```
Desinstalar paquetes (incluyendo archivos de configuración):
```
# sudo aptitude remove –purge <paquetes>
```
Actualizar la lista de paquetes disponibles:
```
# sudo aptitude update
```
Actualizar el sistema con las actualizaciones de paquetes disponibles:
```
# sudo aptitude upgrade
```
Actualiza el sistema borrando e instalando lo que sea necesario:
```
# sudo aptitude dist-upgrade
```
Obtener una lista de opciones del comando:
```
# sudo aptitude help
```
Reinstala el paquete o los paquetes que se indiquen separados por espacios:
```
# sudo aptitude reinstall <paquete1> <paquete2> <paquete3>...
```
Busca un paquete que contenga ese nombre o descripción:
```
# sudo aptitude search <paquete>
```
Muestra la informacion disponible sobre ese paquete:
```
# sudo aptitude show <paquete>
```
Borra (no desisntala) los paquetes descargados que sean redundantes (se quedará con la
última versión):
```
# aptitude autoclean
```
Borra los paquetes descargados:
```
# aptitude clean
```
# Instalar archivos .bin y .sh en Linux
En la ruta donde se encuentre el archivo a instalar, se tendra que darle permisos de ejecución:
```
# sudo chmod a+x nombre_archivo.bin (si se trata de un archivo con
```
extensión .bin)
ó
```
# sudo chmod a+x nombre_archivo.sh (si se trata de un archivo con
extensión .sh)
```
Ejecutar el archivo:
```
# sudo ./nombre_archivo.bin o $ sudo sh nombre_archivo.bin (si se
trata de un archivo con extensión .bin)
```
ó
```
# sudo ./nombre_archivo.sh o $ sudo sh nombre_archivo.sh (si se trata
de un archivo con extensión .sh)
```
# Paquetes deb / rpm
Otra forma de instalar aplicaciones en el sistema es por medio de los paquetes con extensión
.deb.
Para instalar estos paquetes sólo hay que hacer doble click sobre el fichero en el navegador
Nautilus y automáticamente se lanzará la aplicación gdebi, que se ocupará de instalar el
paquete y buscar las dependencias de otros paquetes que pudiera necesitar para su correcta
instalación.
También se pueden instalar mediante la línea de comandos, mediante el comando dpkg:
```
# dpkg -i <paquete>.deb
# rpm -i <paquete>.rpm
```
En este caso también habrá que instalar manualmente las posibles dependencias del paquete.
El mismo comando también se puede usar para desinstalar el paquete:
```
# dpkg -r <paquete>.deb
# rpm -e <paquete>.rpm
```
Para forzar desinstalación paquetes rpm:
```
# rpm -e <paquete>.rpm --force
```


# Convertir paquetes RPM a DebAlgunas distribuciones de GNU/Linux, como por ejemplo Red Hat, SUSE y Mandriva, usan
paquetes .rpm, organizados de manera diferente a los paquetes .deb de Debian y Ubuntu.
Para instalar estos paquetes es preciso convertirlos antes al formato .deb. Para ello se usa la
aplicación alien, la cual se puede instalar mediante uno de los métodos explicados en este
artículo. La aplicación alien se utiliza de la siguiente manera:
```
alien <paquete>.rpm
```
De esta forma el programa crea un archivo con el nombre del paquete, pero con
extensión .deb, que se podrá instalar siguiendo la explicación Paquetes Deb.
