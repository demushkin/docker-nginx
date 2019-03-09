# docker-nginx
Nginx Dockerfile with full config
docker-compose.yml example:

```
version: "3"
services:
    nginx:
        image: demushkin/nginx:latest
        restart: always
        volumes:
            - ../:/var/www
            - ./docker/nginx/sites-enabled:/etc/nginx/sites-enabled
            - ./docker/log/nginx:/var/log/nginx
        ports:
            - "80:80"
        tty: true
}}
```
sites-enabled - directory with you virtual hosts configs
