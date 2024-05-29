# mysql-docker-phpmyadmin
Simple Docker Compose Configuration for phpMyAdmin (MySQL admin tool)

**you need docker and docker compose on your machine**

1. Add your credetials to the docker compose file ([docker-compose.yml](./docker-compose.yml)):
 
```yml
version: '3.7'

services:
  phpmyadmin:
    image: phpmyadmin/phpmyadmin
    container_name: phpmyadmin
    environment:
      PMA_HOST: host-domain.com
      PMA_USER: dbUser
      PMA_PASSWORD: XXXXXX
      PMA_PORT: 3306
    ports:
      - "8080:80"
```

2. Run: `docker-compose up --build`
