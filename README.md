# basic-html-image-docker-compose-master
This is all about how to run a custom html file or a single page in DOCKER

# Basic-HTML-image-docker-compose
You can use [Gshell](https://console.cloud.google.com/) or [labs.play-with-docker](https://labs.play-with-docker.com/) and start playground

## This is just a sample project to run docker-compose with a simple html file.

Here are three files
- Dockerfile
- Docker-compose.yaml
- index.html
```
git clone https://github.com/efxtv/basic-html-image-docker-compose-master.git
```

## For docker build

```
docker build -t imagename .
```


## For running Docker-compose

```
docker run -d -p 80:80 imagename
```

You can change index.html before you push the first command.

Some commands you might find helpful.

- List of running dockers
```
docker images
```

- Stop all the docker containers:
```
docker ps -q|sed 's#^#docker stop #g'|bash
or
ps -q
docker stop dockerid
```

- Remove one or more images
```
docker rmi -f IMAGEID
docker images|awk '{print "docker rmi -f "$3}'|sed '1d'|bash
or
docker rmi REPOSITORY1 REPOSITORY2

```

- Start Docker HTML Page
```
docker build -t imagename .
docker run -d -p 80:80 imagename
```


