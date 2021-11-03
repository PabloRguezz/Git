# Instalación de Git en linux
## Indice
- **[Instalación Predeterminada](#instalación-predeterminada)**
- **[Instalación desde la fuente](#instalación-desde-la-fuente)**
- **[Configuración de Git](#configuración-de-git)**
### Instalación Predeterminada
Para comenzar con esta actividad, primero veremos si nuestra máquina virtual Ubuntu tiene instalado el git. Para ello usaremos el comando **“git --version”**.

<img src="1.png">

En este caso, al no estar instalado deberemos instalarlo, primero realizaremos el update del sistema con **“sudo apt update”**.

<img src="2.png">

Tras realizar el update comenzaremos con la instalación con el comando **“sudo apt install git”**.

<img src="3.png">

Al finalizar la instalación comprobamos que se instaló correctamente con el comando **“git --version”**.

<img src="4.png">

### Instalación desde la fuente 
A continuación, verificaremos la versión de git que hemos instalado anteriormente. Sabemos que es la versión 2.25.1, pero descargamos una versión específica, esta versión será la 2.29.3. Para comenzar realizaremos un update con el comando **“sudo apt update”**. Ahora descargamos las dependencias necesarias para la instalación con el comando **”sudo apt install libz-dev libssl-dev libcurl4-gnutls-dev libexpat1-dev gettext cmake gcc”**.

<img src="5.png">

Tras la descarga crearemos un directorio y nos posicionamos en él. Esto lo haremos con los siguientes comandos. Para la creación del directorio usaremos **“mkdir tmp”** y para ir al directorio usaremos **“cd /tmp”**.

<img src="6.png">

Ahora descargamos la versión que queramos desde el sitio web del proyecto Git. Para esto usaremos el comando curl y lo enviamos a git.tar.gz. Usaremos el siguiente comando **“curl -o git.tar.gz https://mirrors.edge.kernel.org/pub/software/scm/git/git-2.29.3.tar.gz”**.

<img src="7.png">

Descomprimimos el archivo que recientemente hemos descargado con el comando **“tar -zxf git.tar.gz”**.

<img src="8.png">

Tras esto accedemos al nuevo directorio de git con el siguiente comando **“cd git-*”**.

<img src="9.png">

A continuación, creamos el paquete y lo instalamos. Para crear el paquete usamos el comando **“make prefix=/usr/local all”**, y ,para instalar ese paquete, usamos **“sudo make prefix=/usr/local install”**.

<img src="10.png">

<img src="11.png">

Finalmente cambiamos el proceso de shell para que se comience a utilizar la nueva versión de git con el comando **“exec bash”**.

<img src="12.png">

Ya a modo de comprobación usaremos el comando **“git --version”** para ver que se nos ha instalado la nueva versión.

<img src="13.png">

### Configuración de Git

Ya teniendo git instalado podemos realizar su configuración, para realizar la configuracion pondremos el nombre y el correo con los siguientes comandos **“git config --global user.name "Your Name"”** y **“git config --global user.email "youremail@domain.com"”**.

<img src="14.png">

Si queremos ver los datos que hemos creado tendremos que usar el comando **“git config --list”**.

<img src="15.png">

Esta información se guardará en el archivo gitconfig el cual podremos ver y editar con el comando **“nano ~/.gitconfig”**.

<img src="16.png">
