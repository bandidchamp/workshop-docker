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
