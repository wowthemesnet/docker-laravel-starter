# Docker Laravel Starter

#### 1. Clone or download this repository

#### 2. Navigate in project directory

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

#### 8. Useful
- run migrations: `docker-compose exec app php artisan migrate`
- access db PhpMyAdmin: http://localhost:7000

<hr>

#### 9. Credits
- All credits to https://github.com/AngCosmin/docker-laravel 
- Source: [DigitalOcean Community](https://www.digitalocean.com/community/tutorials/how-to-set-up-laravel-nginx-and-mysql-with-docker-compose)
