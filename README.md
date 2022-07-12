## :whale: Aprendiendo Docker

En este repositorio, subiré cada uno de los recursos e información generada durante el seguimiento del [Curso de Docker](https://youtu.be/4Dko5W96WHg) de HolaMundo en YouTube :video_camera:

### :hammer: Instalación
Para la instalación de Docker, mi propósito es instalar la aplicación ***Docker Desktop***.

Visitaré la página web oficial, que contiene los pasos para instalar docker en mi distribución: 

[Docker Desktop](https://docs.docker.com/desktop/linux/install/debian/)

### :pencil: Pasos

~~~
sudo apt remove docker-desktop
~~~

~~~
rm -r $HOME/.docker/desktop
sudo rm /usr/local/bin/com.docker.cli
sudo apt purge docker-desktop
~~~

~~~
sudo apt install gnome-terminal
~~~

~~~
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg lsb-release
~~~

~~~
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
~~~

~~~
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
~~~

~~~
// Descargo el PAQUETE DEB más reciente de Docker Desktop
sudo apt update
sudo apt-get install ./docker-desktop-<version>-<arch>.deb
~~~

#### :open_file_folder: Recursos Importantes :open_file_folder:

:small_orange_diamond: [¿Qué es Docker?](https://www.javiergarzas.com/2015/07/que-es-docker-sencillo.html)

:small_orange_diamond: [Docker Desktop (DD) Oficial](https://docs.docker.com/desktop/linux/install/)

:small_orange_diamond: [DD Instalación rápida Parrot](https://gist.github.com/nuga99/dd5ac250b4c98154b5065d8affec7b49)

:small_orange_diamond: [Instalación respaldo en Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04-es)

:small_orange_diamond: [Error - Command not Found on Debian](https://itsfoss.com/add-apt-repository-command-not-found/)

:small_orange_diamond: [Error - After apt update -> 404 not found IP...](https://es.stackoverflow.com/questions/516243/err11-https-download-docker-com-linux-debian-una-release-404-not-found-ip-5)


