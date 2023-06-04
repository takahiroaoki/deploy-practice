# deploy-practice

## Requirements
The environment is bellow.
- Windows 11
- Docker Desktop for Windows 4.2.0
- VSCode + Remote Development 0.21.0（VSCode extensions）

## Local development
```
$ docker compose build
$ docker compose up -d
$ docker compose exec app /bin/bash
$ sudo npm ci
$ npm run start:dev
```
Then, get access to http://localhost/dev