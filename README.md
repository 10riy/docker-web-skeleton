# Docker skeleton for web application

## Docker Skeleton for web application on NGINX, PHP, POSTGRES, NODEJS

### Installation
Will write down your configuration data
```sh
$ cp .env.example .env
```

Run and  enter in container php
```sh
$ docker-compose up -d
```

### Xdebug
If firewall is enabled
```sh
$ ufw allow in from 172.16.0.0/12 to any port 9000 comment xdebug
```