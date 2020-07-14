# Instalación de Flutter en Ubuntu 20.04 LTS

### 1. SDK
Lo primero que necesitamos es descargar el [SDK](https://flutter-es.io/docs/get-started/install/linux), en este link también puedes encontrar la documentación oficial para instalar flutter. Una vez que tengas descargado el SDK guardalo ya que lo usaremos mas adelante.

### 2. Instalar Git

```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install git
```

Una vez que termina de descargarlo e instalado comprobamos que se instalo correctamente

```
git --version
```

Si esto te regresa alguna versión de git significa que se instalo de manera correcta, en caso contrario antes de continuar con este tutorial busca en Google tu problema y continua una vez que tengas instalado git. Recomiendo esto con todos los siguientes pasos.

### 3. Instalar Java

Como encontré este tutorial que es bastante bueno les dejo el link, el tutorial fue hecho por DigitalOcean y lo encuentras [aqui](https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-on-ubuntu-20-04-es) 

### 4. Instalar Android Studio

##### Usaremos snap

Instalar snap

```
sudo apt install snapd
```

Después lo usamos para instalar Android Studio

```
sudo snap install android-studio --classic
```

Si tienes problemas con esta instalación te dejo el link a un tutorial donde se ven más métodos de instalación [aquí](https://ubunlog.com/android-studio-instalacion-ubuntu/)

### 5. Usaremos el SDK que descargamos previamente

Primero que nada los extraemos 

```
cd ~/Documents
$ tar xf ~/Downloads/flutter_linux_v1.2.1-stable.tar.xz
```
Necesitamos decirle a nuestro Ubuntu donde se encuentra el SDK de flutter

1.Abrimos una terminal
2. ``` cd /home/{usuario actual} ```
3. ```gedit .bashrc ```

Esto nos abrirá un archivo de configuración de Ubuntu, nos iremos hasta el fin de este archivo y agregaremos la siguiente línea

```
export PATH={path-of-sdk}/flutter/bin:$PATH
```
Donde path-of-sdk es la ubicación de donde extrajimos el SDK

Después ejecutamos 

```
echo$PATH
```
Para actualizar el PATH
 
Y en una nueva terminal podremos ejecutar

```
flutter doctor
```
En caso de que no se reconozca el comando flutter, lo más probable es que el PATH del SDK que pusiste en el archivo de configuración está mal, revisa eso. ¡Con eso ya tenemos instalado flutter, a programar!



