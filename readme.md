# Readme
Instructions to seed the docker machine environment (both for dev & production).  Very specific environment via vagrant to setup

   * ubuntu 16.04
   * git tools
   * languages - python
   * docker & docker-compose

# Pre-requisite
On Mac, Vagrant v1.8.6 or above

   * git client
   * python, easy_install, pip `sudo easy_install pip`
   * ansible pkgs `sudo pip install paramiko PyYAML jinja2 httplib2 ansible`

# Instructions
First clone this repository to your box and have pre-requsites installed.

```
   $ cd baremachine
   $ vagrant up
   $ vagrant ssh
```


