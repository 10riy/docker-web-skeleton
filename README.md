# Docker skeleton for web application

## Docker Skeleton for web application on NGINX, PHP, POSTGRES, NODEJS

### Structure project
```
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
├── docker-compose.yml
├── LICENSE.md
└── README.md
```

### Installation
Config for docker in root project folder
```sh
$ cp .env.example .env
```

Create volume for postgres
```sh
$ docker volume create --name app_pgdata -d local
```

Run and  enter in container php
```sh
$ docker-compose up -d
```

