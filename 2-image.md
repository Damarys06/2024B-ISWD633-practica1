# Imagen
Es un archivo único que contiene todos los programas, librerías, dependencias y configuraciones necesarias para instalar y/o ejecutar una aplicación o un conjunto de aplicaciones.
![Imagen](img/imagen.PNG)


## ¿Cuál es la relación entre una imagen y un contenedor? 
Las imágenes y los contenedores de Docker son tecnologías de implementación de aplicaciones. Tradicionalmente, para ejecutar cualquier aplicación en un equipo, era necesario instalar la versión que coincidiera con el sistema operativo de la máquina. Sin embargo, ahora puede crear un solo paquete de software, o contenedor, que se ejecute en todos los tipos de dispositivos y sistemas operativos. Docker es una plataforma de software que empaqueta software en contenedores. Las imágenes de Docker son plantillas de solo lectura que contienen instrucciones para crear un contenedor. Una imagen de Docker es una instantánea o un esquema de las bibliotecas y dependencias necesarias dentro de un contenedor para que se ejecute una aplicación.
# COMPLETAR 

![Imagen y contenedores](img/imagenContenedores.JPG)
## Comandos para imágenes

### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull <nombre imagen> 
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull <nombre imagen>:<tag>
```

Descargar la imagen **hello-world**
![image](https://github.com/user-attachments/assets/e62cbfb6-3fe6-4506-bd61-32c8f8d43e2a)



# COMPLETAR

**¿Qué es nginx**
NGINX, pronunciado en inglés como “engine-ex”, es un famoso software de servidor web de código abierto. En su versión inicial, funcionaba en servidores web HTTP. Sin embargo, hoy en día también sirve como proxy inverso, balanceador de carga HTTP y proxy de correo electrónico para IMAP, POP3 y SMTP.

Este software fue lanzado oficialmente en octubre del 2004. El creador del software, Igor Sysoev, comenzó su proyecto en el 2002 como un intento de solucionar el problema C10k. C10k es el reto de gestionar diez mil conexiones al mismo tiempo.

# COMPLETAR 

Descargar la imagen  **nginx** en la versión **alpine**
![image](https://github.com/user-attachments/assets/79c4820c-f70e-41ee-8b42-0937fc003ff6)


# COMPLETAR

### Listar imágenes

```
docker images
```
![image](https://github.com/user-attachments/assets/63728214-ee65-44f1-89f7-251b49f9abd5)

# COLOCAR UNA CAPTURA DE PANTALLA DEL RESULTADO 

**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 
![image](https://github.com/user-attachments/assets/3251ca2a-26ee-4505-a295-aa200880dd5f)

# COMPLETAR

**¿Con qué algoritmo se está generando el ID de la imagen**
{
        "Id": "sha256:d211f485f2dd1dee407a80973c8f129f00d54604d2c90732e8e320e5038a0348",
        "RepoTags": [
            "hello-world:latest"
        ],
# COMPLETAR

### Filtrar imágenes

```
docker images | grep <termino a buscar>

```

### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi <nombre imagen>:<tag>
```

Eliminar la imagen hello-world 
![image](https://github.com/user-attachments/assets/f8548ed7-00c1-459f-9726-bae691406a37)


# COMPLETAR

-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```

