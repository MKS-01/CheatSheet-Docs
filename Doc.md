## HomeBrew <img src='https://cdn.svgporn.com/logos/homebrew.svg'  height="42" width="42"/>

```shell
 $ brew update && brew upgrade
```

<hr/>


## Docker <img src='https://cdn.svgporn.com/logos/docker-icon.svg' height="auto" width="42" />

#### Container?

A container is simply another process on your machine that has been isolated from all other processes on the host machine. That isolation leverages kernel namespaces and cgroups, features that have been in Linux for a long time. Docker has worked to make these capabilities approachable and easy to use.

```shell
$ docker run -d -p 80:80 docker/docker-name
```
- -d - run the container in detached mode (in the background)
- -p 80:80 - map port 80 of the host to port 80 in the container
- docker/docker-name - the image to use

Shorten

```shell
$ docker run -dp 80:80 docker/getting-started
```