
# cadasta-platform

[![Build Status](https://travis-ci.org/Cadasta/cadasta-platform.svg?branch=master)](https://travis-ci.org/Cadasta/cadasta-platform)


### Install for development

- [VirtualBox](https://www.virtualbox.org/)
- [Vagrant](https://www.vagrantup.com/)
- [Ansible](https://www.ansible.com/)


###For Linux
      sudo apt-get update
      sudo apt-get install virtualbox
      sudo apt-get install dkms
      sudo apt-get install vagrant
      pip install ansible

dkms (optional): "Ubuntu/Debian users might want to install the dkms package to ensure that the VirtualBox host kernel modules (vboxdrv, vboxnetflt and vboxnetadp) are properly updated if the linux kernel version changes during the next apt-get upgrade."<br>
In case , your are behind proxy or facing connection timed out issue while installing you should switch to pip3 8.2.1 + version for installing development environment.

###For Macs
      brew cask install virtualbox
      brew cask install vagrant
      brew cask install vagrant-manager
      pip install --user --upgrade ansible
Vagrant-Manager helps you manage all your virtual machines in one place directly from the menubar.



