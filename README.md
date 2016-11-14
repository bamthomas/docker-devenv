# docker-devenv

This is a "minimal" dev environment including java : 
* dev user with sudo without password
* git 
* mounting X
* mounting docker socket

It is based on [phusion/baseimage](https://github.com/phusion/baseimage-docker) for a good init process and syslog/ssh to work properly.

To use it, build your image with :

    $ docker build -t your_image_name .
    $ export MY_IMAGE=your_image_name
    $ export MY_HOME=`pwd` # for example
    $ docker-compose up -d
    Creating dockerjava_dev_1
    $ ./enter_dev_docker.sh dockerjava_dev_1
    
