# Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Ensure that Docker is Running](#ensure-that-docker-is-running)
- [Using Python Notebooks](#using-docker-for-python-notebooks)
- [Using R Notebooks](#using-docker-for-r-notebooks)

## Introduction

*Contain Yourself*  provides volunteers of DataKind Singapore a consistent enviroment when working on a project. By containerizing our tools we can:

- be inclusive of volunteers who are running Windows/MacOS/Linux
- be more productive by reducing frictions in working on different platforms
- maintain reproducibility when sending containers with code to our partners as it's ready to run no matter what environment they're using.

### What are containers (in the software sense)?

Containers are a virtual operating system that can run applications or processes the same way regardless of the actual host operating system. For example, somebody who has Windows installed on their laptop can:

1. develop an application within a container
2. pass that container to her project members
3. run the application on their machines regardless of their operating system
4. get the same results from running the application

We'll be using [Docker](https://www.docker.com/) containers. Docker images for different projects will be hosted in a Quay.io repository. [Quay.io](https://quay.io/) is a service that specializes in building and hosting Docker repositories.

## Installation

### ... for Windows

Follow the setup instructions here: https://docs.docker.com/docker-for-windows/install/

Note: If your machine doesn't met the requirement for "Docker For Windows", try setting up "Docker Toolbox":
https://docs.docker.com/toolbox/toolbox_install_windows/

### ... for Linux

Follow the setup instructions for your flavor of Linux here: https://docs.docker.com/engine/installation/linux/

### ... for MacOS

Follow the setup instructions here: https://store.docker.com/editions/community/docker-ce-desktop-mac

Or if you use Homebrew Cask,

```
$ brew cask install docker
```

## Ensure that Docker is Running

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

## Using Docker for Python Notebooks
### Getting a Python Jupyter Notebook Container Image

There are at least two ways of getting an image:

- Pulling from a repository (such as quay.io)
- Loading from a file

#### Pulling from a repository
You can pull down the image with:

```
$ docker pull quay.io/dksg/python3-notebook:1.0.0
```

Once that finishes downloading, you should see something like:

```
$ docker images
REPOSITORY                      TAG                 IMAGE ID            CREATED             SIZE
quay.io/dksg/python3-notebook   1.0.0              f01e49a5a922        3 days ago          2.61 GB
```

#### Loading from a file
This is an alternative method. Skip this if you already have pulled from a repository successfully. Otherwise, follow the steps below:

1. Copy the tar file (get this from a DK corelead) to your local directory (e.g. quay.io_SLASH_dksg_SLASH_python3-notebook_1.0.0.tar)
2. In your local directory, run the following docker command:
```
docker load --input quay.io_SLASH_dksg_SLASH_python3-notebook_1.0.0.tar
```
3. This will return a loaded image id.
4. Tag the newly added image with the version from the filename by running the following:
```
docker tag <loaded image id> quay.io/dksg/python3-notebook:1.0.0

```

### Running a Jupyter Notebook from the pulled/loaded image

Take the `IMAGE ID` from previous step and start it up with this command:

```
docker run -it -p 8888:8888 -v /path/to/local/directory:/home/jovyan/work f01e49a5a922
```
**Note:** /path/to/local/directory should be replaced by **an existing local directory in your laptop.**
This is where your notebooks (.ipynb) will be stored.
e.g. docker run -p 8888:8888 -v /Users/johndoe/datadive:/home/jovyan/work quay.io/dksg/python3-notebook:1.0.0

You will get instructions for link to paste into your browser address box. If you're using Docker Toolbox, you should use the custom IP address (default http://192.168.99.100/)

### Once the notebook is running, you may create a new notebook and try the samples in this tutorial:
https://plot.ly/python/ipython-notebook-tutorial/


## Using Docker for R Notebooks
### Getting an R Jupyter Notebook Container Image

There are at least two ways of getting an image:

- Pulling from a repository (such as quay.io)
- Loading from a file

#### Pulling from a repository
You can pull down the image with:

```
$ docker pull quay.io/dksg/r-notebook:1.0.1
```

Once that finishes downloading, you should see something like:

```
$ docker images
REPOSITORY                      TAG                 IMAGE ID            CREATED             SIZE
quay.io/dksg/r-notebook   1.0.1              f01e49a5a922        3 days ago          2.61 GB
```

#### Loading from a file
This is an alternative method. Skip this if you already have pulled from a repository successfully. Otherwise, follow the steps below:

1. Copy the tar file (get this from a DK corelead) to your local directory (e.g. quay.io_SLASH_dksg_SLASH_r-notebook_1.0.1.tar)
2. In your local directory, run the following docker command:
```
docker load --input quay.io_SLASH_dksg_SLASH_r-notebook_1.0.1.tar
```
3. This will return a loaded image id.
4. Tag the newly added image with the version from the filename by running the following:
```
docker tag <loaded image id> quay.io/dksg/r-notebook:1.0.1

```

### Running a Jupyter Notebook from the pulled/loaded image

Take the `IMAGE ID` from previous step and start it up with this command:

```
docker run -it -p 8888:8888 -v /path/to/local/directory:/home/jovyan/work f01e49a5a922
```
**Note:** /path/to/local/directory should be replaced by **an existing local directory in your laptop.**
This is where your notebooks (.ipynb) will be stored.
e.g. docker run -p 8888:8888 -v /Users/johndoe/datadive:/home/jovyan/work quay.io/dksg/r-notebook:1.0.1

You will get instructions for link to paste into your browser address box. If you're using Docker Toolbox, you should use the custom IP address (default http://192.168.99.100/)

### Once the notebook is running, you may create a new notebook and try the following samples:
https://plot.ly/r/using-r-in-jupyter-notebooks/#examples
