# What

laravel-admin (https://github.com/z-song/laravel-admin) starter kit by docker-compose.

# setup

```bash
$ cp ./.env.example ./.env
$ docker compose build admin
$ docker compose run --rm admin composer install
$ docker compose run --rm admin php artisan key:generate
$ docker compose run --rm admin php artisan admin:publish
$ docker compose run --rm admin php artisan migrate
$ docker compose run --rm admin php artisan db:seed --class=AdminTablesSeeder
$ docker compose run --rm admin php artisan admin:create-user # create an admin user with username and password
$ docker compose up admin
```

Then open http://localhost:8000/admin with your browser.

![screenshot](https://user-images.githubusercontent.com/69618840/170651081-9fd64fe0-0a06-4cdd-a499-e3eb69366bef.png)

# File generate command

```bash
$ docker-compose run --rm admin php artisan make:model Api/User # Generate User model
$ docker-compose run --rm admin php artisan admin:make UserController --model=App\\Models\\Api\\User # Generate User Controller
$ docker-compose run --rm admin php artisan admin:action User\\Import --name="import" # Generate csv import action
```

