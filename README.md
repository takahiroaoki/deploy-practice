# deploy-practice

## Requirements
The environment is bellow.
- Windows 11
- Docker Desktop for Windows 4.2.0
- VSCode + Remote Development 0.21.0（VSCode extensions）

## Local development
```
$ docker compose -f docker-compose.dev.yml build
$ docker compose -f docker-compose.dev.yml up -d
$ docker compose -f docker-compose.dev.yml exec app /bin/bash
$ sudo npm ci
$ npm run start:debug
```
Then, get access to http://localhost/dev

When you stop docker containers.
```
$ docker compose -f docker-compose.dev.yml stop
```

## Deploy [Work In Progress]
```
$ docker compose -f docker-compose.prod.yml build
$ docker compose -f docker-compose.prod.yml up -d
```