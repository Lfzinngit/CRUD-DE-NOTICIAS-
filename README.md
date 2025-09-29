# CRUD-DE-NOTICIAS-

PROJETO LARAVEL 
CÓDIGOS VIA BASH:

composer create-project laravel/laravel laravel-breeze-sqlite
cd laravel-breeze-sqlite

mkdir database
touch database/database.sqlite

composer require laravel/breeze --dev
php artisan breeze:install
npm install && npm run dev
php artisan migrate

php artisan make:model Noticia -m

php artisan migrate

php artisan make:controller NoticiaController --resource --model=Noticia

php artisan make:policy NoticiaPolicy --model=Noticia
