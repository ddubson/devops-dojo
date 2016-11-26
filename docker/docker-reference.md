### Data Containers

Containers responsible for storing and handling data. They do not run like traditional containers.

Usually come in the following steps:
* Create a simple image 

`docker create -v <mounted-data> --name <container-name> <image-name>`

* Copy over data from fs to the image 

`docker cp <local-file> <container-name>:<mounted-data>`

* Run the container that depends on the data container, the data container will automatically
map the volumes in the data container to the image.

`docker run --volumes-from <data-container-name> <image-name>`

### Docker Ignore

`.dockerignore` files are used to exclude files or directories
to be included in the final docker image that is built

It is based on `.gitignore` premise.