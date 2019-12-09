# Ubuntu 18.04, Docker installation
from https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04

  - Install Ubuntu Server 18.04
  - sudo apt update
  - sudo apt upgrade -y



sudo apt install apt-transport-https

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"

sudo apt update

Check if Docker is available from repository

apt-cache policy docker-ce

docker-ce:
  Installed: (none)
  Candidate: 18.03.1~ce~3-0~ubuntu
  Version table:
     18.03.1~ce~3-0~ubuntu 500
        500 https://download.docker.com/linux/ubuntu bionic/stable amd64 Packages

sudo apt install docker-ce

sudo systemctl status docker

sudo usermod -aG docker ${USER}

sudo reboot (or logout)

su - ${USER}

id -nG

If you need to add a user to the docker group that you're not logged in as, declare that username explicitly using: sudo usermod -aG docker username
