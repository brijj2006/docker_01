build image from dockerfile and assign the name and the respective tag
- docker build -t docker-test:v1 .

list down all the images in docker
- docker images

create docker container from the above image listening to port 7000 locally exposed to port 80 from docker file.
delete the container once the docker container is stopped, give name to docker container
- docker run -p 7000:80 --rm --name dockerapp docker-test:v1

get the list of active docker containers
- docker ps

get the list of all docker containers
- docker ps -a

create docker container which is not deleted once it stops
- docker run -p 7000:80 --name dockerapp docker-test:v1

stop and start docker app
- docker stop dockerapp
- docker start dockerapp

rename docker image
- docker tag docker-test:v1 brijj2006/docker-test

login to dockerhub
- docker login

logout from dockerhub
- docker logout

push a docker image to docker hub : for pushing the image to the repo, one should be logged in to dockerhub
- docker push brijj2006/docker-test

pull images from dockerhub : for pulling the image from the repo, no need to be logged in to dockerhub
- docker pull brijj2006/docker-test:latest