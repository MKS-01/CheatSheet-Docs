## Homebrew <img src='https://cdn.svgporn.com/logos/homebrew.svg'  height="42" width="42"/>

```shell
$ brew install --cask file

$ brew update && brew upgrade
```

<hr/>


## Docker <img src='https://cdn.svgporn.com/logos/docker-icon.svg' height="auto" width="42" />

#### Container?
A container is simply another process on your machine that has been isolated from all other processes on the host machine. 

##### Run

```shell
$ docker run -d -p 80:80 docker/docker-name
```
- -d - run the container in detached mode (in the background)
- -p 80:80 - map port 80 of the host to port 80 in the container
- docker/docker-name - the image to use

###### Shorthand

```shell
$ docker run -dp 80:80 docker/docker-name
```

##### Building the App's Container Image

1. Create a file named ```Dockerfile```

```shell
FROM node:12-alpine
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]
```

2. Build the container image using the ```docker build``` command.

```shell
$ docker build -t docker-name .
```
   
The ```-t``` flag tags image. The ```.``` at the end of the ```docker build``` command tells that Docker should look for the ```Dockerfile``` in the current directory.

##### Starting an App Container

```shell
$ docker run -dp 3000:3000 docker-name
```

##### Removing a container

```shell
$ docker ps  #get id of container

$ docker stop <the-container-id> # Swap out <the-container-id> with the ID from docker ps

$ docker rm <the-container-id>

```

###### Shorthand
```shell
$ docker rm -f <the-container-id>
```

##### Create a Volume

```shell
$ docker volume create volume-name
#mount volume
```

##### Inspect a Volume

```shell
$ docker volume inspect volume-name
```

##### Check Logs

```shell
$ docker logs -f <container-id>
```

## NVM <img src='https://cdn.svgporn.com/logos/nodejs-icon.svg' height="42" width="42" />


```shell
#generate a .nvmrc file 
$ node -v > .nvmrc

$ nvm ls  #check node version installed on machine

$ nvm install --lts

$ nvm install node

$ nvm use node_version

$ nvm uninstall node_version

```
