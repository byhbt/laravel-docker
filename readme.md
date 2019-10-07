
## Laravel Docker
- Adminer: it's simple than PHPMyAdmin.
But because of IPV6 problem, so I use version *4.2.5* https://github.com/TimWolla/docker-adminer/issues/40

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
Application Homepage
```bash
http://localhost:8989
```

Adminer
```bash
http://localhost:8990
```

Username: root
Password: secret

You can edit these info in the **docker-compose.yml**

## FAQ
1. File permission problem:
Ref: [If you are running Docker on Linux, the files created are owned by root.](https://docs.docker.com/compose/django/)

```bash
sudo chown -R $USER:$USER .
```

## References:

https://qiita.com/dyoshikawa/items/63a974b5aee488b080f8

## Contributing

Free to make pull request. 

