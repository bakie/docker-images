# docker-images
This repository holds all my dockerfiles for different operating systems.

## Table of contents
* [Supported Operating Systemts](#supported-operating-systems)
    * [Debian](#debian)
    * [Ubuntu](#ubuntu)
* [Adding new image to docker hub](#adding-new-image-to-docker-hub)

### Supported Operating Systems
#### Debian
* [stretch](debian-stretch)
* [buster](debian-buster)

#### Ubuntu
* [bionic beaver](ubuntu-bionic-beaver)
* [focal fossa](ubuntu-focal-fossa)

### Testing it locally
To test it locally before building it on docker hub, simply run the following inside the directory where the Dockerfile is located.
```
$ docker image build -t ${NAME} .

E.g. $ docker image build -t focal-fossa .
```

### Adding new image to docker hub
When creating a new docker image, this must also be configured in [docker hub](https://hub.docker.com).
Go to bakie/docker-images repository > builds, and click configure automated builds. 
Add a new build rule and fill in the required fields. Make sure to fill in the correct docker tag and build context. 
The tag will be used when you need to pull in a specific docker image and the build context is 
the path to the correct Dockerfile.