# Principales comandos de docker 

### Manejo de imagenes 

- Creaciòn de imagenes en el directorio en el que te encuentras 

`
  docker build . 
`

- Creaciòn de una imagen con tag especifico 

`
 docker build -t [tag] . 
`

- Muestra todas la imagenes s

`
 docker images 
`

- Corre una imagne con el id o tag 

`
 docker run [tag o id]
`

- Corre una imagen con el id o tag de la imagen junto con una  consola 
    
`
 docker run -it [tag o id] [cmd]
`
