##### Search for an image in registry
`docker search <image-name>`

##### Copy file/dir to container
`docker cp <local-file> <container-name>:<directory>`

### Running Containers

##### Run container with an exposed port
`docker run -p <host-port>:<container-port> <image-name>`

##### Run container with a local volume mapped to the container
`docker run -v <host-dir>:<container-dir <image-name>`

##### Run container with an environment variable
`docker run -d -e [ENV_VAR]=[VAR_VALUE]`

##### Run container with a custom DNS entry
```bash
docker run -i --dns=8.8.8.8 --name=mycontainer1 -i ubuntu:latest
```

###
```bash
docker run -t --dns=8.8.8.8 --dns-search=mydomain.local --volume /local_vol --volume /home/user:/remote_vol --name=mycontainer3 -i ubuntu:latest /bin/bash
```

##### Mount volume hosting basic web template
```bash
docker run --name=webtest -v /home/ddubson/docker/dockerwww:/var/www/html -it centos6:baseweb /bin/bash
```

###
```bash
docker run -d -i -t --name=devweb1 -p 8081:80 -v /home/ddubson/docker/dockerwww:/var/www/html centos6:finalweb1 /bin/bash
```

### Building Images
##### Build image
`docker build -t <image-name>:<version> <directory-of-Dockerfile>`