# Laravel boilerplate - Kiwi

Packages

-   Git
-   Tailwind
-   Blueprint
-   Filament

Instalación y preparación de desarrollo.

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

## Seed user admin demo:

```sh
$ sail php artisan migrate:refresh --seed

# name : Kiwi admin
# email : kiwi@admin.com
# password : kiwipass

# Optional generate users panel
$ sail php artisan make:filament-resource User --generate
```

## Livewire / inertiajs ?

## Language?
