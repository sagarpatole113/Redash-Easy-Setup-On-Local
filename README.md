# Redash-Easy-Setup-On-Local
Redash setup on local

Enable windows subsystem for linux

-- dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

Enable Virtual Machine feature

-- dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

Download the Linux kernel update package

-- wsl.exe --install or wsl.exe --update

Set WSL 2 as your default version

-- wsl --set-default-version 2

Install your Linux distribution from Microsoft Store

Install Docker on Linux 

-- sudo apt-get -qqy update

-- sudo apt-get -y install apt-transport-https ca-certificates curl software-properties-common wget pwgen

-- curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

-- sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

-- sudo apt-get update && sudo apt-get -y install docker-ce

-- sudo systemctl start docker

-- sudo systemctl status docker

-- sudo docker --version

--sudo curl -L https://github.com/docker/compose/releases/download/1.22.0/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose

-- sudo chmod +x /usr/local/bin/docker-compose

-- sudo docker-compose --version

Clone setup repository

-- https://github.com/getredash/setup.git

Get inside setup repository

-- cd setup

Make the script executable

-- chmod +x setup.sh

Run setup.sh file

-- ./setup.sh

Give user access to docker

-- sudo usermod -aG docker $USER

Check if docker containers are up and running

-- sudo docker ps


If all containers are running go to browser and hit

http://localhost:5000/


