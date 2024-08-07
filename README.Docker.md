# Docker Overview

## Docker Setup

This project uses Docker and Docker Compose to manage the development environment.


<br>

## Installation Guide

### **Install Docker**
Follow the instructions on the [Docker website](https://docs.docker.com/get-docker/) to install Docker for your operating system.

### **Install Docker Compose**
Docker Compose is included with Docker Desktop for Windows and macOS. For Linux, follow the instructions on the [Docker Compose installation page](https://docs.docker.com/compose/install/).

<br>

## Commands: Managing Containers and Images

### **View all containers**
```sh
docker ps -a -q
```

### **Clean all containers**
Removes all existing Docker Containers globally
```sh
docker container rm -f $(docker container ls -a -q)
```

### **View all images**
```sh
docker images -a -q
```

### **Clean all images**
Removes all existing Docker Images globally

```sh
docker image rm -f $(docker image ls -a -q)
```

<br>

## Commands: Building and Running Environment

### **Build New Environment**
This will cleanly build all Containers and Images and
```sh
docker-compose build --no-cache --force-rm
```

### **Run Environment**
This will cleanly build all Containers and Images and
```sh
docker-compose up -d
```

### **Shut Down and Save Containers**
This will cleanly build all Containers and Images and
```sh
docker-compose stop
```

### **Shut Down Containers**
This will cleanly build all Containers and Images and
```sh
docker-compose down
```

<br>

## Commands: Connecting to Environment

### **Connect to Container**
```sh
docker-compose exec <container> <command>
```

<br>
