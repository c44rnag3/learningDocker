## :whale: Aprendiendo Docker

En este repositorio, subiré cada uno de los recursos e información generada durante el seguimiento del [Curso de Docker](https://youtu.be/4Dko5W96WHg) de HolaMundo en YouTube :video_camera:

### :hammer: Instalación
Para la instalación de Docker, mi propósito es disponer de la aplicación ***Docker Desktop***.

Visitaré la página web oficial, que contiene los pasos para instalar docker en mi distribución: 

*Mi distribución* :cd: **Parrot 5.0.1 Electro Ara (Home Edition)** - :x: *Antigua*

*Mi distribución* :cd: **Ubuntu Desktop 20.04.4 LTS** - :heavy_check_mark: *Actual*

[Docker Desktop](https://docs.docker.com/desktop/linux/install/debian/)

#### :pencil: Pasos

~~~
sudo apt remove docker-desktop
~~~

~~~
rm -r $HOME/.docker/desktop
sudo rm /usr/local/bin/com.docker.cli
sudo apt purge docker-desktop
~~~

~~~
sudo rm -r ~/.config/systemd/user/docker-desktop.service
sudo rm -r ~/.local/share/systemd/user/docker-desktop.service
~~~

~~~
sudo apt install gnome-terminal
~~~

~~~
sudo apt update
sudo apt install -y curl apt-transport-https ca-certificates gnupg lsb-release software-properties-common
~~~

~~~
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
echo "deb [arch=amd64] https://download.docker.com/linux/debian stretch stable" | sudo tee /etc/apt/sources.list.d/docker-engine.list
~~~

~~~
// Descargo el PAQUETE DEB más reciente de Docker Desktop
sudo apt update
sudo apt install ./docker-desktop-<version>-<arch>.deb
~~~

Me aseguro de que la instalación se ha llevado a cabo correctamente:

~~~
docker compose version
// salida -> Docker compose version vX.X.X...
~~~
~~~
docker --version
// salida ->  Docker version XX.XX.XX, build...
~~~
~~~
docker version
// salida -> Client: XX... / Cloud Integration...
~~~

### :rocket: Puesta en marcha y Funcionamiento
*Iniciar Docker Desktop*
~~~
systemctl --user start docker-desktop
~~~

*Habilitar que se inicie Docker Desktop al iniciar sesión*
~~~
systemctl --user enable docker-desktop
~~~

*Detener Docker Desktop*
~~~
systemctl --user stop docker-desktop
~~~

*Comprobar estado (Funcionamiento) Docker Desktop*
~~~
systemctl --user status docker-desktop
~~~


#### :open_file_folder: Recursos Importantes :open_file_folder:

:small_orange_diamond: [¿Qué es Docker?](https://www.javiergarzas.com/2015/07/que-es-docker-sencillo.html)

:small_orange_diamond: [Docker Desktop (DD) Oficial](https://docs.docker.com/desktop/linux/install/)

:small_orange_diamond: [DD Instalación rápida Parrot](https://gist.github.com/nuga99/dd5ac250b4c98154b5065d8affec7b49)

:small_orange_diamond: [Instalación respaldo en Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04-es)

:small_orange_diamond: [Error - Command not Found on Debian](https://itsfoss.com/add-apt-repository-command-not-found/)

:small_orange_diamond: [Error - After apt update -> 404 not found IP...](https://es.stackoverflow.com/questions/516243/err11-https-download-docker-com-linux-debian-una-release-404-not-found-ip-5)

:small_orange_diamond: [apt-key is deprecated (1)](https://stackoverflow.com/questions/68992799/warning-apt-key-is-deprecated-manage-keyring-files-in-trusted-gpg-d-instead)

:small_orange_diamond: [apt-key is deprecated (2)](https://techviewleo.com/apt-key-is-deprecated-manage-keyring-files-in-trusted-gpg-dot-d/)
