# Docker for php developers
Inspired by http://www.newmediacampaigns.com/blog/docker-for-php-developers

## commands used:

### docker
docker build -t docker-4-php-devs/nginx .

docker images

docker pull nmcteam/php56

docker pull --disable-content-trust=true nmcteam/php56

docker pull sameersbn/mysql

docker run \
    -d \
    -p 8080:80 \
    -v $(pwd)/src/vhost.conf:/etc/nginx/sites-enabled/vhost.conf \
    -v $(pwd)/src:/var/www \
    docker-4-php-devs/nginx;

docker ps

docker stop [CONTAINER ID]

docker rm [CONTAINER ID]

docker exec -it [CONTAINER_ID] /bin/bash

### docker-compose

docker-compose up -d

docker-compose logs
