stop the existing docker images and remove them

use: docker-compose down

docker rm susanazou/bsz_tech:openfree-web-img

docker rm susanazou/bsz_tech:openfree-service-img

docker rm susanazou/bsz_tech:openfree-db-img

then run the new docker-compose

docker-compose -f docker-compose-production.yml up -d

Then check the logs for docker containers

docker exec -it deploy-openfree-sql bash
docker logs deploy-openfree-sql
docker logs deploy-openfree-web
docker logs deploy-openfree-service

in addition, make sure you can connect to the following in a browser in a different machine

http://66.76.242.195:8080/category
http://66.76.242.195:3000
