# Docker

## Concepts

## Comands

### Basic comands

#### Hello world!
To run our first container in docker (e.g. a Hello world! container) the only thing we must run in the CLI is: `docker run hello-world`

#### Runing hello world container for second time
When we run many more times the previous command, docker will create a container for each sentence sent in the CLI. It's important mention that each new "Hello world!" container will take a new name.

#### Creating a container with an specific name
`docker run --name <nameContainer> hello-world`

#### Rename a container
`docker rename <previousNameContainer> <newNameContainer>`

#### List our containers
`docker ps` command will show the active containers, not the finished. If we want to see all the containers, including the finished, we must type `docker ps -a`

#### Inspect an specific container
`docker inspect <idContainer>`

#### Deleting an specific container
`docker rm <nameContainer>`

-f after "rm" stops the container before being deleted

#### Deleting all the containers 
`docker container prnue`


#### Detener un contenedor
`docker stop <nameContainer>`


### Mediums commands

#### Detach (Dejar corriendo un contenedor en segundo plano)

`docker run -d --name proxy nginx`

#### Exponiendo puertos

`docker run --name <nameContenedor> -d -p [puertoAnfitrion:puertoContenedor] <imagen>`

Mapea el puerto del contenedor con el puerto de la maquina anfitriona, en el ejemplo anterior, si se accede al navegador y se escribe: http://localhost:8080 estaremos viendo lo que el contenedor expone en su puerto 80

#### Ver logs del contenedor

`docker logs -f <nombreContenedor>`

la -f es de follow

#### Ver ultimas lineas de algo (p. e. logs)

`docker logs --tail 10 -f <nombreContenedor>`

El anterior muestra las ultimas 10 lineas de los logs. No muestra todos

### Manejo de datos en docker

