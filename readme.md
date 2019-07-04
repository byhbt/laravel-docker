
## Laravel Docker
- Docker compose 3.3 syntax
- Adminer supported.

## How to use

Step 1:

Install docker and docker-compose to your pc.

Step 2:

Clone code repository then install dependencies:
```
git clone
npm install
composer update
```

Build docker images
```
docker-compose build
docker-compose up -d
```

```bash
chmod -R 777 storage
```

Running php artisan:

```bash
docker-compose exec php php artisan migrate
```

## Access the app and services
Web application 
```bash
http://localhost:8080
```

Redis Commander
```bash
http://localhost:8081
```

Adminer
```bash
http://localhost:8082
```

Username: root
Password: secret

You can edit these info in the **docker-compose.yml**

## Contributing

Free to make pull request. 
