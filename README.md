# Transaction Service environment

Backend: Laravel MariaDB PHP 

Frontend: TypeScript React 

Server: Nginx

Environment: Docker

## Postman documentation links

[Authorization documentation](https://documenter.getpostman.com/view/31412589/2sAYkLmbvx)

[Main operations documentation](https://documenter.getpostman.com/view/31412589/2sAYkLmbw2#d46ae33b-8ab1-455a-8dc5-f4a138a4a3b7)


To run the transaction service,  run the following command:

Structure of the project:

    ├── README.md
    ├── docker-compose.yml
    ├── transaction-service-backend
    ├── transaction-service-frontend

To run the transaction service,  run the following command:


##  Installation

### Clone the repository
```sh
git clone --recurse-submodules https://github.com/your-name/transaction-service-environment.git
```

### Prepare Laravel environment
```sh
cp transaction-service-backend/.env.example transaction-service-backend/.env
```

### Start Docker containers
```sh
docker-compose up --build -d
```

### Install PHP dependencies
```sh
docker-compose exec transaction-service-backend composer install
```

### Generate Laravel key
```sh
docker-compose exec transaction-service-backend php artisan key:generate
```

### Run migrations
```sh
docker-compose exec transaction-service-backend php artisan migrate
```

### Run seeders
```sh
docker-compose exec transaction-service-backend php artisan db:seed
```

### If you want to run queue worker
```sh
docker-compose exec transaction-service-backend php artisan queue:work

```

#### Backend local installation finished







