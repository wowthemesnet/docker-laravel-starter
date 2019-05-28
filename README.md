# Docker Laravel Starter

Basic Laravel setup with Docker:
- MySQL
- PHPMyAdmin
- NGINX
- Composer
- Voyager Admin


#### 1. Clone this repository

`git clone https://github.com/wowthemesnet/docker-laravel-starter.git`

#### 2. Navigate in project directory

`cd docker-laravel-starter`

#### 3. Composer install
On Linux/MacOS: `docker run --rm -v $(pwd):/app composer install`  
On Windows in PowerShell: `docker run --rm -v ${PWD}:/app composer install`  
On Windows in CMD: `docker run --rm -v %cd%:/app composer install`  

#### 4. Create .env file
`cp .env.example .env`  

#### 5. Start everything
`docker-compose up`  

#### 6. Generate key for Laravel application
`docker-compose exec app php artisan key:generate`  

#### 7. Access
Enter on http://localhost  

#### Useful Tasks
- run migrations: `docker-compose exec app php artisan migrate`    
- access db PhpMyAdmin: http://localhost:7000

#### 8. Install Voyager Admin

- run the following to install Voyager Admin:

    On Linux/MacOS: `docker run --rm -v $(pwd):/app composer require tcg/voyager`  
    On Windows in PowerShell: `docker run --rm -v ${PWD}:/app composer require tcg/voyager`  
    On Windows in CMD: `docker run --rm -v %cd%:/app composer require tcg/voyager`

- `docker-compose exec app php artisan voyager:install --with-dummy`
- `docker-compose exec app php artisan vendor:publish --provider="TCG\Voyager\VoyagerServiceProvider"`
- `docker-compose exec app php artisan vendor:publish --provider="Intervention\Image\ImageServiceProviderLaravel5"`

- Access Voyager account: http://localhost/admin 

    User: admin@admin.com
    Pass: password

<hr>

#### Credits
- Credits and many thanks to [AngCosmin](https://github.com/AngCosmin/docker-laravel)
- Source: [DigitalOcean Community](https://www.digitalocean.com/community/tutorials/how-to-set-up-laravel-nginx-and-mysql-with-docker-compose)

<hr>

#### Enjoy and visit [me](https://www.wowthemes.net)