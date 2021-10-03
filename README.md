# demodocker

### Sample Docker File:
FROM ubuntu
RUN apt-get update
RUN apt-get install -y nginx
COPY index.nginx-debian.html /var/www/html
CMD nginx -g 'daemon off;'


### Other Commands:

docker build .

docker run -dt -p 80:80 nginx
* runs detached in the background (stays running)
* Port on machine 80 : port to container 80

docker run -dt -p 8090:80 nginx
* Port on machine 8090 : port to container 80

docker run -it –name=Test_1 ubuntu
* will run ubuntu container interactively 

docker exec -it containername /bin/bash
* gets you to the shell /bin/bash of the docker container.
