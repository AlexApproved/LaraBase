## Docker Setup

This project uses Docker and Docker Compose to manage the development environment.

### Installation Guide

1. **Install Docker**:
    - Follow the instructions on the [Docker website](https://docs.docker.com/get-docker/) to install Docker for your operating system.

2. **Install Docker Compose**:
    - Docker Compose is included with Docker Desktop for Windows and macOS. For Linux, follow the instructions on the [Docker Compose installation page](https://docs.docker.com/compose/install/).

### Common Docker Commands

- **Build containers**:
    ```sh
      docker-compose build --no-cache --force-rm
    ```

- **Start containers**:
    ```sh
    docker-compose up --detach
    ```

- **Stop containers**:
    ```sh
    docker-compose stop
    ```

- **Remove containers**:
    ```sh
    docker-compose down
    ```

- **connect to container**:
    ```sh
    docker exec -it laravel-app bash
    ```

- **Execute commands in the app container**:
    ```sh
    docker-compose exec <container> <command>
    ```

- **View running containers**:
    ```sh
    docker ps
    ```

- **View logs**:
    ```sh
    docker-compose logs
    ```

### Common Issues

- **Container not starting**:
    - Ensure Docker is running.
    - Check the logs for errors using `docker-compose logs`.

For more details on Docker usage, refer to the [official documentation](https://docs.docker.com/).
