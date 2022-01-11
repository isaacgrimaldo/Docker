# Practica 01

En esta practica crearemos un servidor nginx para mostras un simpe web site

### Lista de comandos

- Corremos el servidor de nginx con docker y le pasamos el contenido del web site 

`
 $ docker run --name website -p 5000:80 -d  -v  $(pwd):/usr/share/nginx/html:ro nginx 
`

 --name se le pone nombre al conetendor

 -p Los puertos de configuracion 

 -d Ejecutarlo fuera de la shell actual

 -v Funcion para servir los documentos del web site pero debe tener  correctamente las localizacion de donde estan los documentos y la direcion dentro del servidor donde leeran los documentos (-v  $(pwd):/usr/share/nginx/html:ro)

 :ro funciona para que solo se pueda leer los documetos

 $(pwd) solo funcionara si ejecutas el comando directamente en la carperta donde tienes el web site de lo contrario tendras que escribirlo


- Entramos al contendor con el siguien comando 

`
 $ docker exex -it website bash 
`

- Creamos un nuevo documento en la carpeta donde esta todo el html del servidor 

~~~~
  cd usr/share/nginx/html 

  touch services.html
~~~~

De esta forma tambien podermos hacer cambios desde el contendor y estos se veran reflejados en el directorio raiz del proyecto


