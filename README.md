# Laravel boilerplate - Kiwi

## Despues de clonar el repo que hacer:

```sh
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
