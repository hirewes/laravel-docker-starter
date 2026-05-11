# Laravel Docker Setup

## Start Docker Containers

Start all containers in detached mode:

```bash
docker-compose up -d
```

---

## Enter the Laravel PHP Container

Access the `php_laravel` container:

```bash
docker exec -it php_laravel bash
```

---

## Create a New Laravel Project

Inside the container, create a new Laravel project in the current directory:

```bash
composer create-project laravel/laravel .
```

---

## Set Laravel Permissions (Optional)

```bash
chmod -R 775 storage bootstrap/cache
```

---

## Setup Environment File

Copy the example environment file:

```bash
cp .env.example .env
```

Generate the Laravel application key:

```bash
php artisan key:generate
```

---

## Verify Laravel Installation

Check the installed Laravel version:

```bash
php artisan --version
```

---

## Open Laravel in Browser

```text
http://localhost
```