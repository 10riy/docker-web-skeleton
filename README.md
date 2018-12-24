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
Will write down your configuration data
```sh
$ cp .env.example .env
```

Run and  enter in container php
```sh
$ docker-compose up -d
```

