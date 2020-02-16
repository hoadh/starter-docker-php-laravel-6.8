# README

## Prepare

* docker
* docker-compose

## Clone & Install

```shell script
git clone https://github.com/hoadh/starter-docker-php-laravel-6.8.git

# Install without composer
docker run --rm -v $(pwd):/app prooph/composer:7.3 install
```

```shell script
docker-compose up -d
cp .env.example .env

# Generate key và optimze command:
docker-compose exec app php artisan key:generate
docker-compose exec app php artisan cache:clear

# Optional:
docker-compose exec app php artisan migrate:fresh
```

## Run

* Open http://0.0.0.0:8080/
* Start coding!
