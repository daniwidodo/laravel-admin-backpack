- Install Laravel

- Install Laravel Breeze - api
composer require laravel/breeze --dev
php artisan breeze:install api
npm install
npm run dev
php artisan migrate

- Install Laravel Backpack
# require Backpack using Composer
composer require backpack/crud:"4.1.*"
composer require --dev backpack/generators

# run the installation command
php artisan backpack:install

- Generate CRUD
-- https://backpackforlaravel.com/docs/4.1/getting-started-basics
# STEP 1. create a migration
php artisan make:migration:schema create_tags_table --model=0 --schema="name:string:unique,slug:string:unique"
php artisan migrate

# STEP 2. create a CRUD for it
php artisan backpack:crud tag #use singular, not plural