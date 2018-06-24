docker run -it -d --name docker-web -p 9000:9000 docker.io/uifd/ui-for-docker 

docker run -it -d --name docker-web -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock docker.io/uifd/ui-for-docker 

