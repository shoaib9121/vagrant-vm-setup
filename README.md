# Virtual Machine, Vagrant, Docker setup guide

## Install Vagrant

- Download and Install Oracle Virtual Box from official [website](https://www.virtualbox.org/wiki/Downloads).
- Navigate to this link https://www.vagrantup.com/downloads.html page and download/install the Vagrant package.
- Once Oracle Virtual Box is installed make sure to restart the machine.

## Setup Docker via Vagrant Box

- `vagrant box add gusztavvargadr/docker-linux`
- `mkdir docker && cd docker`
- 'vagrant init gusztavvargadr/docker-linux` (this will create Vagrantfile in current directory)
- Change VM network to public. `nano Vagrantfile` and look for line `config.vm.network "public_network"` and uncomment it.
- `vagrant up`
- Select Wifi (wireless) network. Enter a corresponding digit against Wifi connected.
- `vagrant ssh` (to enter into vagrant shell)

## Setup Docker without Vagrant Box

- `sudo apt-get update`
- `sudo apt-get install curl`
- `curl -fsSL https://get.docker.com -o get-docker.sh`
- `sh get-docker.sh`
- `sudo usermod -aG docker $USER`
