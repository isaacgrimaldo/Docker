# Principales comandos de docker 

## Creacion de Imagnes

- Creaciòn de imagenes en el directorio en el que te encuentras 

`
  $ docker build . 
`

- Creaciòn de una imagen con tag especifico 

`
 $ docker build -t [tag] . 
`
<hr/>

## Manejo de Imagenes

- Muestra todas la imagenes que existen en el sistema

`
 $ docker images 
`

- Corre una imagne con el id o tag 

`
 $ docker run [tag o id]
`

- Corre una imagen con el id o tag de la imagen junto con una  consola 
    
`
 $ docker run -it [tag o id] [cmd]
`

- Borrar imagenes

`
 $ docker rmi [id o name] 
`

- Borrar todas las imagenes

`
$ docker rmi $(docker images -aq)
`



<hr/>

## Descaragar Recursos desde Docker-Hub

Para descargar una imagen primero debes ir a [Docker-Hub](https://hub.docker.com) y buscar la imagen que quieres descargar y leer sobres esta. 

- Descargar una imagen 

`
 $ docker pull [imageName]
`

- Buscar imagenes desde consola 

`
 $ docker search [imageName]
`


<hr/>

## Contenedores

Los contenedores son las intancias de la imagenes, puedes correr cientos, miles de contenedores apatir de una imagen 

- Mostrar por consola todo los contendores corriendo en el sistema 

`
 $ docker ps
`

- Muestra en consola todos los contendores existentes en el sistema

`
 $ docker ps -a 
`

- Correr un contenedor por su id

`
 $ docker start [id] o [three first letter from id]
`

- Correr un contendor con cambiando el puerto  y  la carga en consola

`
 $ docker run -p [newPort]:[DefaultPort] -d [id o  imageName]
`

- Correr multiples contenedores al mimsmo tiempo

`
docker run (-p [newPort]:[DefaultPort]) x each container -d [image] 
`

- Correr una contenedor con un nombre especifico 

`
  docker run --name [SetName] [image]
`

- Corre un contenedor con variables de entorno (Exemplo con MySQL)

`
dokcer run  --name mydatabase  -p 3000:3306  -d  -e [Enviroment Variable]=[value] [image]
`

En el caso de mysql tu puedes buscar en la documentacion de la imagen  [mysql](https://hub.docker.com/_/mysql) aqui podemos sutituir [Enviroment Variable]=[value] por una varible de la docuentacion quedaria asi 

`
 $ docker run -p 3000:3306 --name mydatabase -a -e MYSQL_ROOT_PASSWORD=1234567752 mysql 
`

- Borrar todos los contenedores  

`
 $docker rm (docker ps -aq) -f  
`


<hr/>

