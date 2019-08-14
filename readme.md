# API Laravel Passport

API documentation [here](https://documenter.getpostman.com/view/6336991/SVYwMHME) in postman

## Table of Contents

- [Installation](#installation)
- [Dependencies](#dependencies)
- [Routes](#routes)
    - [Authentication](#authentication)
    - [Password Reset](#password-reset)


### Installation

1. Clone repository
```
$ git clone https://github.com/raj4rachit/laravel-passport-api.git
```

2. Enter folder
```
$ cd laravel-passport-api
```

3. Install composer dependencies
```
~/laravel-passport-api$ composer install
```

4. Generate APP_KEY
```
~/laravel-passport-api$ php artisan key:generate
```

5. Configure .env file, edit file with next command `$ nano .env`
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=database
DB_USERNAME=user
DB_PASSWORD=secret
```

6. Run migrations
```
~/laravel-passport-api$ php artisan migrate
```

7. Create client
```
~/laravel-passport-api$ php artisan passport:install
```


### Dependencies


- [laravolt/avatar](https://github.com/laravolt/avatar) - Generate avatars for users of application


### Routes

##### Authentication

- POST /auth/login
- GET /auth/logout
- POST /auth/signup
- GET /auth/signup/activate/{token}
- GET /auth/user


##### Password Reset

- POST /password/create
- GET /password/find/{token}
- POST /password/reset
