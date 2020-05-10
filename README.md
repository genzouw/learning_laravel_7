# Learning laravel 7

## Requirements

* Docker

## Create Application

```bash
APP_NAME=exif_json

docker \
  run --rm -v $PWD:/workdir --workdir=/workdir \
  composer \
  create-project --prefer-dist laravel/laravel "${APP_NAME}"

cd "${APP_NAME}"
```

## Launch develop server

```bash
docker \
  run --rm -v $PWD:/workdir --workdir=/workdir \
  -d \
  -p 8000:8000 \
  php:7.3-cli \
  php artisan serve --host=0.0.0.0
```
