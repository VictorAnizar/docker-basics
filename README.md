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