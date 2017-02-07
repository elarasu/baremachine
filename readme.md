# Readme
Instructions to seed the docker machine environment (both for dev & production).  Very specific environment via vagrant to setup

   * ubuntu 16.04
   * git tools
   * languages - python
   * docker & docker-compose

# Pre-requisite
none

# Instructions
First clone this repository to your box and have pre-requsites installed.

```
   $ cd baremachine
   $ vagrant up
   $ vagrant ssh
```
## Update
On updates to vagrantfile, please run the following instructions
```
   $ cd baremachine
   $ vagrant halt
   $ vagrant up
   $ vagrant provision
   $ vagrant ssh
```
