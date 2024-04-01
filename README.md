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

# Copiar los enviroments
$ cp .env.example .env
# el archivo .env generado se puede cambiar segun sus preferencias

# Para trabajar con vite
$ sail npm run dev

# Para compilar vite
$ sail npm run build

# Expone los archivos de solo para docker
$ sail php artisan storage:link

# Migraciones de bases de datos
$ sail php artisan migrate:refresh --seed

# Optional generate users panel
$ sail php artisan make:filament-resource User --generate
```

Login con el usuario: (database/seeders/DatabaseSeeder.php) es necesario haber corrido las migraciones y el seed:

-   name : Kiwi admin
-   email : kiwi@admin.com
-   password : kiwipass

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
