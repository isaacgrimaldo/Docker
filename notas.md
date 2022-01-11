# Notas sobre la creaciòn de imagenes 


### DockerFile

Este documento en donde escribieron las principales caracteristicas de la imagen que vamos a crear, 


### Docker Image

- Es una plantilla para el  proyecto 

- Contiene todos lo elementos que necesita la app para correr

- puede tener multiples versiones 

- Son creadas usando el DockerFfile 

-  Las imagenes creadas no se pueden modificar 

-  Se puede clonar las imagenes

Si corrers una imagen que no tienes instalada localmenten docker automaticamente la descargara por ti, eso si,  tienes que escribir corrertamente el nombre de la imagen como se encuentras en [Docker-Hub](https://hub.docker.com)

### Contenedores 

- Cuando se corre una imagen de lo que se crea es un contenedor (Corre una instancia de la imagen)

- Corre igual los programas como si fueran instalados nativamente 

todos los contenedores tienen un id uncio que ayuda a docker a indentficar los si es que son requeridos por ti, puedes usar el id completo o solo las tres primeras letras 
