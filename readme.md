# Readme
Instructions to seed the docker machine environment (both for dev & production).  Very specific environment via vagrant to setup

   * ubuntu 15.04
   * git tools
   * languages - python
   * docker & docker-compose

# Pre-requisite
On Mac, Vagrant v1.6.3 or above

   * git client
   * python, easy_install, pip `sudo easy_install pip`
   * ansible pkgs `sudo pip install paramiko PyYAML jinja2 httplib2 ansible`

# Instructions
First clone this repository to your box and have pre-requsites installed.

```
   $ cd vagrant-ubuntu-docker
   $ vagrant up
   $ vagrant ssh
```


