
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

###For Windows
You can download setup files for [VirtualBox](https://www.virtualbox.org/wiki/Downloads) and [Vagrant](https://www.vagrantup.com/downloads.html) respectively and run it. Setup wizard is straightforward, just it will ask to accept license agreement and the path to install, as you will need to use command line.
Windows isn’t supported for the control machine. Go through  ansible [docs](http://docs.ansible.com/ansible/intro_windows.html).
[Here](https://www.jeffgeerling.com/blog/running-ansible-within-windows) is the steps for getting ansible running on Windows:

- Download and install [Cygwin](http://cygwin.com/install.html), with at least the following packages selected (you can select the packages during the install process):
	- curl
	- python (2.7.x)
	- python-jinja
	- python-crypto
	- python-openssl
	- python-setuptools
	- git (1.7.x)
	- vim
	- openssh
	- openssl
	- openssl-devel
- If you are working behind a proxy (as is the case in many corporate networks), edit the .bash_profile used by Cygwin either using vim (open Cygwin and enter `vim .bash_profile`), or with whatever editor you'd like, and add in lines like the following:
	
        export http_proxy=http://username:password@proxy-address-here:80/
        export https_proxy=https://username:password@proxy-address-here:80/
- Download and install [PyYAML](https://pypi.python.org/pypi/PyYAML/3.10) and [Jinja2](https://pypi.python.org/pypi/Jinja2/2.6) separately, as they're not available via Cygwin's installer:
	-  Open Cygwin
	-  Download PyYAML:

		    curl -O https://pypi.python.org/packages/source/P/PyYAML/PyYAML-3.10.tar.gz
	- Download Jinja2:
	
		    curl -O https://pypi.python.org/packages/source/J/Jinja2/Jinja2-2.6.tar.gz
	- Untar both downloads:
	
		    tar -xvf PyYAML-3.10.tar.gz && tar -xvf Jinja2-2.6.tar.gz
	- Change directory into each of the expanded folders and run `python setup.py install` to install each package.
    - Generate an SSH key for use later: `ssh-keygen`, then hit enter to skip adding a password until you get back to the command prompt.
    - Clone ansible from its repository on GitHub:
    
		    git clone https://github.com/ansible/ansible /opt/ansible
   - If you'd like to work from a particular Ansible version (like 2.0.1, current as of this writing), change directory into `/opt/ansible` and checkout the correct tag: `git checkout v2.0.1` (some users have also reported success with the tag `v2_final`).

   - Add the following lines into your Cygwin `.bash_profile` (like you did the proxy settings—if you're behind one—in step 2):

		    # Ansible settings
		    ANSIBLE=/opt/ansible
		    export PATH=$PATH:$ANSIBLE/bin
		    export PYTHONPATH=$ANSIBLE/lib
		    export ANSIBLE_LIBRARY=$ANSIBLE/library
		    

   - At this point, you should be able to run ansible commands via Cygwin (once you restart, or enter `source ~/.bash_profile` to pick up the settings you just added). Try `ansible --version` to display Ansible's version.
 
If you using Windows 10's Subsystem for Linux refer to this [blog](https://www.jeffgeerling.com/blog/2017/using-ansible-through-windows-10s-subsystem-linux)



