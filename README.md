# workshop-docker

# docker command
## - build image frontend-app
docker build -t frontend-app -f Dockerfile.frontend .

## - build image backend-app
docker build -t backend-app -f Dockerfile.backend .

## - run container frontend-app
docker run --name frontend-app -p 80:80 frontend-app:latest

## - run container backend-app
docker run --name backend-app -p 3001:3001 backend-app:latest

## - stop container frontend-app
docker stop frontend-app

## - stop container backend-app
docker stop backend-app

## - remove image frontend-app
docker rmi -f frontend-app

## - remove image backend-app
docker rmi -f backend-app

## - list image
docker images

## - list container
docker ps -a


## docker-compose
## - run container
docker-compose up -d

## - rebuild
docker-compose up -d --build

## - down container 
docker-compose down 

## deploy google cloud run [backend app]
1. run cmd: gcloud init
2. set gcloud project
3. run cmd: cd backend-app
4. run cmd: gcloud builds submit --tag asia.gcr.io/mpk-covid/workshop-docker-backend
5. setup cloud run 


## deploy google cloud run [frontend app]
1. run cmd: gcloud init
2. set gcloud project
3. run cmd: cd frontend-app
4. run cmd: gcloud builds submit --tag asia.gcr.io/mpk-covid/workshop-docker-frontend
5. setup cloud run 

container image url:
asia.gcr.io/mpk-covid/workshop-docker-backend@sha256:0be12229294ee6dd8c93ad9ff28630d87c5e5dea30917d50f2265779078f6e41 -> asia.gcr.io/mpk-covid/workshop-docker-backend:latest

:: server build images
gcloud init

:: cmd - deploy backend-app
gcloud builds submit --tag asia.gcr.io/training-355603/workshop-backend-app-champ

:: cmd - deploy frontend-app
gcloud builds submit --tag asia.gcr.io/training-355603/workshop-frontend-app-champ


:: local build images
:: cmd docker build

docker build -t asia.gcr.io/training-355603/workshop-backend-app-docker-champ .

:: cmd docker push images

docker push asia.gcr.io/training-355603/workshop-backend-app-docker-champ

ถ้า push ไม่ได้ให้รันคำสั่งนี้

gcloud auth configure-docker

สวัสดีภาษาไทย