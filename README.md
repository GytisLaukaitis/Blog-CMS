## Build Blog CMS (Content Management System) with Laravel 7

## Clone this repo
```
https://github.com/GytisLaukaitis/Blog-CMS.git
```

## Install composer packages
```
$ cd laravel-7-blog-cms
$ composer install
$ php artisan ui bootstrap --auth
$ npm install
$ npm run dev
```

## Create and setup .env file
```
make a copy of .env.example and rename to .env
$ php artisan key:generate
put database credentials in .env file
```

## Migrate and insert records
```
$ php artisan migrate
$ php artisan tinker
$ factory(App\User::class, 5)->create();
$ factory(App\Post::class, 100)->create();
$ exit
$ php artisan db:seed --class=CategoriesTableSeeder
$ php artisan tinker
$ factory(App\CategoryPost::class, 100)->create();
```

## Use storate images
```
$ php artisan storage:link
```

## Use Docker
```
Config your .env file to

DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laraapp_db
DB_USERNAME=root
DB_PASSWORD=


$ docker-compose up -d
$ docker ps   (to find ID of a project)
$ docker exec -it (project ID) bash
$ composer install

If you run into errors

$ php artisan route:clear
$ php artisan config:clear
$ php artisan cache:clear

Run migrations
```

## Mail setup 

visit at : https://mailtrap.io/
put mail credentials in .env file
```

