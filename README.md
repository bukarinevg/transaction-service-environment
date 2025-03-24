# Transaction Service environment

To run the transaction service,  run the following command:

Structure of the project:

    ├── README.md
    ├── docker-compose.yml
    ├── transaction-service-backend
    ├── transaction-service-frontend

To run the transaction service,  run the following command:


## Prepare Laravel environment
```sh
cp transaction-service-backend/.env.example transaction-service-backend/.env
```

## Start Docker containers
```sh
docker-compose up --build -d
```

## Install PHP dependencies
```sh
docker-compose exec transaction-service-backend composer install
```

## Generate Laravel key
```sh
docker-compose exec transaction-service-backend php artisan key:generate
```

## Run migrations
```sh
docker-compose exec transaction-service-backend php artisan migrate
```
