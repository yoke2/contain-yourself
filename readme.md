# Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Using Docker](#using-docker)

## Introduction

*Contain Yourself*  provides volunteers of DataKind Singapore a consistent enviroment when working on a project. By containerizing our tools we can be:

- inclusive of volunteers who are running Windows/MacOS/Linux
- more productive by reducing frictions in working on different platforms
- reproducible by sending containers with code to our partners, ready to run no matter what environment they're using

### What are containers (in the software sense)?

Containers are a virtual operating system that can run applications or processes the same way regardless of the actual host operating system. For example, somebody who has Windows installed on their laptop can:

1. develop an application within a container
2. pass that container to her project members
3. run the application on their machines regardless of their operating system
4. get the same results from running the application

We'll be using [Docker](https://www.docker.com/) containers. Docker images for different projects will be hosted in a Quay.io repo. [Quay.io](https://quay.io/) is a service that specializes in hosting private Docker repositories.

## Installation

### ... for Windows

Follow the setup instructions here: https://docs.docker.com/docker-for-windows/install/

### ... for Linux

Follow the setup instructions for your flavor of Linux here: https://docs.docker.com/engine/installation/linux/

### ... for MacOS

Follow the setup instructions here: https://docs.docker.com/docker-for-mac/install/

Or if you use Homebrew Cask,

```
$ brew cask install docker
```

## Using Docker

Start running the Docker app. Check that it is running on the command line:

```
$ docker info
Containers: 3
 Running: 0
 Paused: 0
 Stopped: 3
Images: 1
Server Version: 1.13.1
...
```

### Jupyter Python Notebook

You can pull down the image with:

```
$ docker pull quay.io/dksg/python3-notebook
```

Once that finishes downloading, you should see something like:

```
$ docker images
REPOSITORY                      TAG                 IMAGE ID            CREATED             SIZE
quay.io/dksg/python3-notebook   latest              f01e49a5a922        3 days ago          2.61 GB
```

Take that `IMAGE ID` and start it up with this command:

```
docker run -it -p 8888:8888 -v /path/to/local/directory:/home/jovyan/work f01e49a5a922
```

You will get instructions for link to paste into your browser address box. If you're using Docker Toolbox, you should use the custom IP address (default http://192.168.99.100/)

Note: /path/to/local/directory would be the path to the directory in where you store your .ipynb

### Jupyter R Notebook

You can pull down the image with:

```
$ docker pull quay.io/dksg/r-notebook
```

Once that finishes downloading, you should see something like:

```
$ docker images
REPOSITORY                      TAG                 IMAGE ID            CREATED             SIZE
quay.io/dksg/r-notebook   latest              0fd93ce8a437        3 days ago          2.63 GB
```

Take that `IMAGE ID` and start it up with this command:

```
docker run -it -p 8888:8888 -v /path/to/local/directory:/home/jovyan/work 0fd93ce8a437
```

You will get instructions for link to paste into your browser address box. If you're using Docker Toolbox, you should use the custom IP address (default http://192.168.99.100/)

Note: /path/to/local/directory would be the path to the directory in where you store your .ipynb
