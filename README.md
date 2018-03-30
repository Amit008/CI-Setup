# CI-Setup
Installing and Configuring Multiple Continuous Integration support

Setup Source Code Repository:
I'm using Gitlab community edition for this Exercise:
  --Docker is Pre-installed if not follow the link based on your OS
  https://docs.docker.com/install/
  
  --download gitlab community edition docker image from gitlab docker hub
  --run docker command to pull the docker image:
    docker pull gitlab/gitlab-ce
  
  --Modify the volume location as per your base os location: 
    sudo docker run --detach \
    --hostname gitlab.example.com \
    --publish 443:443 --publish 80:80 --publish 22:22 \
    --name gitlab \
    --restart always \
    --volume /srv/gitlab/config:/etc/gitlab \
    --volume /srv/gitlab/logs:/var/log/gitlab \
    --volume /srv/gitlab/data:/var/opt/gitlab \
    gitlab/gitlab-ce:latest
