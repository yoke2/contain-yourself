# Contents

- [Introduction](#introduction)
- [Installation](#isntallation)

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

We'll be using [Docker](https://www.docker.com/) containers. Docker images for different projects will be hosted in this repo. [Insert explanation of quay.io]

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
