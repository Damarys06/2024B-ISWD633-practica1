# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine

![image](https://github.com/user-attachments/assets/a541e9df-9bf8-40c3-bb7d-2b37ca803128)

# COMPLETAR
Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world
![image](https://github.com/user-attachments/assets/e51b84e1-9b8d-4792-bf84-1d68da7738c5)


# COMPLETAR

### Listar los contenedores ejecutándose o no

```
docker ps -a
```
![image](https://github.com/user-attachments/assets/7362911a-33be-4140-8344-ee511e00b44a)

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 
# COMPLETAR
![image](https://github.com/user-attachments/assets/c9bd3743-80b4-44c0-b614-80787a6fc33e)

### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```
![image](https://github.com/user-attachments/assets/6cf34eb1-9a23-4d39-a816-ccedb1030474)


### Para detener un contenedor

```
docker stop <nombre contenedor>
```

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](img/dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
![image](https://github.com/user-attachments/assets/36c63b00-817c-44ae-99ef-6a5d01a0d3b2)


# COMPLETAR

**¿Qué sucede luego de la ejecución del comando?**

Se inicializa orrectamente y se inician múltiples procesos de trabajo para manejar el tráfico web entrante.

# COMPLETAR  

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
# COMPLETAR

![image](https://github.com/user-attachments/assets/1b9cafb8-2021-4fb1-8ad7-09ba359d26bf)

### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
# COMPLETAR
![image](https://github.com/user-attachments/assets/3de9ec22-a25e-42ae-9573-5a28d7fb3894)

Verificar que el contenedor que se eliminó
# COMPLETAR
![image](https://github.com/user-attachments/assets/36dfcfd6-c727-40fb-b64d-4509103b07d9)

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 
![image](https://github.com/user-attachments/assets/be0fda90-9ac0-4b16-831b-2730709240c2)

# COMPLETAR

Verificar que el contenedor que se eliminó

![image](https://github.com/user-attachments/assets/5c41b550-854c-43c1-91a8-c6c1bbb79919)

# COMPLETAR

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
![image](https://github.com/user-attachments/assets/0498b7ac-03b3-4417-b3e8-41ea6e55be3a)


# COMPLETAR


