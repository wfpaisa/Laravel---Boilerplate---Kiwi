# Laravel boilerplate - Kiwi

## Despues de clonar el repo que hacer:

```sh
# Iniciar contenedores de docker
$ docker-compose up -d

# Remplazar [Laravel-Boilerplate-Kiwi-laravel.test-1] por el nombre del contenedor
# Nota:
#    - Ver nombres de contenedores con: docker ps -a  (el que tenga un nombre de contenedor con la palabra laravel)
#    - Esto generara la carpeta vendors
$ docker exec Laravel-Boilerplate-Kiwi-laravel.test-1 composer install

# Bajar contenedores y volumenes importante, de lo contrario
# puede generar problemas de permisos en directorios
$ docker-compose down -v

# Copiar los enviroments
# Nota:
#    - El archivo .env generado se puede cambiar segun sus preferencias
$ cp .env.example .env

# De aqui en aldelante para iniciar los contenedores usar
$ sail up -d

# Expone los archivos en docker, esto permite que se puedan ver los archivos por laravel
$ sail php artisan storage:link

# Migraciones de bases de datos
$ sail php artisan migrate:fresh --seed

# Iniciar proyecto npm
$ sail npm i
$ sail npm run build

# En el navegador se puede ver en http://localhost

# Opcional Para trabajar con vite
$ sail npm run dev

# Optional generate users panel
$ sail php artisan make:filament-resource User --generate

# Opcional vscode, deshabilitar la extension por defecto de php
# buscar en extensiones: @builtin php
# y la deshablitar exteción llamada: PHP Language Features
```

### Panel admin

Entrar con la url: http://localhost/panel-admin

-   name : Kiwi admin
-   email : kiwi@admin.com
-   password : kiwipass

Nota:
Para el login con el usuario es necesario haber corrido las migraciones y el seed.
(database/seeders/DatabaseSeeder.php) contiene los datos del usario.

## Que tiene instalado:

Packages

-   Git
-   Tailwind
-   Blueprint
-   Filament
-   Vs Code config

Comandos:

```bash
# 1. Init laravel docker
curl -s https://laravel.build/kiwi | bash

# 2. Git
$ git init && git add . && git commit -m 'init'

# 3. Tailwind
# Use the guide: https://tailwindcss.com/docs/guides/laravel#vite
# with sail... example: sail npm install -D tailwindcss postcss autoprefixer

# 4. Blueprint
$ sail composer require -W --dev laravel-shift/blueprint

# 5. Filament
$ sail composer require filament/filament:"^3.2" -W
$ sail php artisan filament:install --panels
```

## Livewire / inertiajs ?

## Language?
