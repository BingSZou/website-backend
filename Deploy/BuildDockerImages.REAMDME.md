Build docker images

Pre-Req: make sure website_backend and website_frontend are populated.  
then run the following in terminal. This assumes the docker images will be pushed susanazou account.

docker login -u susanazou

cd website-backend
docker build -f Deploy/Dockerfile_Db -t susanazou/bsz_tech:openfree-db-img ./database
docker push susanazou/bsz_tech:openfree-db-img

Build service docker images:
docker build -f Deploy/Dockerfile -t susanazou/bsz_tech:openfree-service-img ./
docker push susanazou/bsz_tech:openfree-service-img

---

cd website-frontend
docker build -t susanazou/bsz_tech:openfree-web-img
susanazou/bsz_tech:openfree-web-img
