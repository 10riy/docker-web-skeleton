# Docker Skeleton for web application on NGINX, PHP, POSTGRES, NODEJS

## Structure project
.
├── docker  # Docker files
│   ├── nginx
│   │   ├── Dockerfile
│   │   └── ...
│   ├── node
│   │   ├── Dockerfile
│   │   └── ...
│   ├── php
│   │   ├── Dockerfile
│   │   └── ...
│   └── postgresql
│       ├── Dockerfile
│       └── ...
├── src  # Source code
│   └── ...
├── docker-compose.yml
├── Makefile
├── CHANGELOG.md
└── README.md

### Installation
Config for docker in root project folder
```sh
$ cp .env.example .env
```

Create volume for postgres
```sh
$ docker volume create --name pgdata -d local
```

Run and  enter in container php
```sh
$ docker-compose up -d
```

