# docker-tools
Just a compilation of useful docker tools/information

## Portainer

Portainer is a container which gives a nice ui dashboard to use docker easily. We’ll create and run the portainer container like below

`$ sudo docker run -d --name portainer -p 8888:9000 -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer`

Above will create a container from portainer image and then run it in background ( -d flag make the container run in background). The command will search for the portainer image in local machine and if it doesn’t find the image then it will pull the image from docker image registry. We’ll run the container in port 9000 so port 9000 should be available, but if you want to use any other port than specify it via the -p flag ( -p 8080:9000 ). Also notice that we have named our container portainer with — name flag. You can name your container whatever you want. When the download is complete we can check that the container is running by $ docker ps command. It’ll show a list of all the running container.

Info taken from https://medium.com/@searching.nehal/setting-development-environment-for-laravel-with-docker-8c564899ac08
