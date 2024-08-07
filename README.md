
<p align="center">
    <a href="https://laravel.com" target="_blank">
        <img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo">
    </a>
</p>

# Laravel Docker Starter Template

## Features
This starter template includes the following services:
- **Laravel**
- **PHP 8.3**
- **MySQL**
- **phpMyAdmin**
- **Mailpit**
- **Node.js**
- **NPM**
- **Vite**
- **Redis**

## Prerequisites
Ensure you have the following installed on your system:
- [Docker](https://docs.docker.com/engine/install/) (stable version)
- [Docker Compose](https://docs.docker.com/compose/install/#install-compose) (compatible version)

## Setup Instructions

### Initial Setup
Follow these steps the first time you set up the project:
1. Build and launch the Docker containers:
    ```bash
    docker compose up -d --build
    ```
2. Set the correct permissions for phpMyAdmin sessions:
    ```bash
    docker compose exec phpmyadmin chmod 777 /sessions
    ```
3. Access the PHP container:
    ```bash
    docker compose exec php bash
    ```
4. Modify ownership and permissions for the necessary directories:
    ```bash
    chown -R www-data:www-data /var/www/storage /var/www/bootstrap/cache
    chmod -R 775 /var/www/storage /var/www/bootstrap/cache
    ```
5. Complete the Laravel setup:
    ```bash
    composer setup
    ```

### Subsequent Starts
For future startups, simply run:
- Start the Docker containers:
    ```bash
    docker compose up -d
    ```

## Accessing Services

### Laravel Application
- **URL**: [http://localhost](http://localhost)

### Mailpit
- **URL**: [http://localhost:8025](http://localhost:8025)

### phpMyAdmin
- **URL**: [http://localhost:8080](http://localhost:8080)
- **Server**: `db`
- **Username**: `data`
- **Password**: `data`
- **Database**: `data`

## Essential Docker Commands
Here are some basic Docker Compose commands for managing your environment:
- **Build or rebuild services**:
    ```bash
    docker compose build
    ```
- **Start and run containers**:
    ```bash
    docker compose up -d
    ```
- **Stop and remove containers, networks, etc.**:
    ```bash
    docker compose down
    ```
- **Stop all running services**:
    ```bash
    docker compose stop
    ```
- **Restart specific services**:
    ```bash
    docker compose restart
    ```
- **Execute a command inside a running container**:
    ```bash
    docker compose exec [container] [command]
    ```

## Handy Laravel Commands
Use these Laravel Artisan commands for common tasks:
- **Show basic information about the app**:
    ```bash
    php artisan about
    ```
- **Clear the configuration cache**:
    ```bash
    php artisan config:clear
    ```
- **Clear the application cache**:
    ```bash
    php artisan cache:clear
    ```
- **Clear all cached events and listeners**:
    ```bash
    php artisan event:clear
    ```
- **Clear the queue**:
    ```bash
    php artisan queue:clear
    ```
- **Clear the route cache**:
    ```bash
    php artisan route:clear
    ```
- **Clear compiled view files**:
    ```bash
    php artisan view:clear
    ```
- **Clear compiled classes**:
    ```bash
    php artisan clear-compiled
    ```
- **Clear cached bootstrap files**:
    ```bash
    php artisan optimize:clear
    ```
- **Clear the scheduler's cached mutex files**:
    ```bash
    php artisan schedule:clear-cache
    ```
- **Flush expired password reset tokens**:
    ```bash
    php artisan auth:clear-resets
    ```

---

This version maintains the same information but presents it with varied text and structure for better differentiation.
