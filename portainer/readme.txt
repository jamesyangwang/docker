docker volume create portainer_data
#linux
#docker run -d -p 9000:9000 --name portainer --restart always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer
#windows git bash
#docker run -d -p 9000:9000 --name portainer --restart always -v /var/run/docker.sock:/var/run/docker.sock -v C:\ProgramData\Portainer:C:\data portainer/portainer
#docker run -d -p 9000:9000 --name portainer --restart always -v portainer_data:/data portainer/portainer -H tcp://localhost:2375
#docker run -d -p 9000:9000 --name portainer --restart always -v portainer_data:/data portainer/portainer
docker run -d -p 9000:9000 portainer/portainer
