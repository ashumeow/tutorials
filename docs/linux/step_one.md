+++
title = "Install Docker"
description = "Getting started with Docker"
keywords = ["beginner, tutorial, Docker"]
[menu.linux]
identifier = "linux_install"
weight = 1
+++

# Install Docker

1. Log into your Ubuntu installation as a user with `sudo` privileges.

2. Verify that you have `wget` installed.

        $ which wget

    If `wget` isn't installed, install it after updating your manager:

        $ sudo apt-get update
        $ sudo apt-get install wget

3. Get the latest Docker package.

        $ wget -qO- https://get.docker.com/ | sh

    The system prompts you for your `sudo` password. Then, it downloads and
    installs Docker and its dependencies.
    
    >**Note**: If your company is behind a filtering proxy, you may find that the
    >`apt-key`
    >command fails for the Docker repo during installation. To work around this,
    >add the key directly using the following:
    >
    >       $ wget -qO- https://get.docker.com/gpg | sudo apt-key add -

4. Verify `docker` is installed correctly.

        $ docker run hello-world
        Unable to find image 'hello-world:latest' locally
        511136ea3c5a: Pull complete
        31cbccb51277: Pull complete
        e45a5af57b00: Pull complete
        hello-world:latest: The image you are pulling has been verified.
        Important: image verification is a tech preview feature and should not be
        relied on to provide security.
        Status: Downloaded newer image for hello-world:latest
        Hello from Docker.
        This message shows that your installation appears to be working correctly.

        To generate this message, Docker took the following steps:
        1. The Docker client contacted the Docker daemon.
        2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
           (Assuming it was not already locally available.)
        3. The Docker daemon created a new container from that image which runs the
           executable that produces the output you are currently reading.
        4. The Docker daemon streamed that output to the Docker client, which sent it
           to your terminal.

        To try something more ambitious, you can run an Ubuntu container with:
        $ docker run -it ubuntu bash

        For more examples and ideas, visit:
        http://docs.docker.com/userguide/
  
## Where to go next

At this point, you have successfully installed Docker. Leave the terminal window
open. Then, go onto [read a very short explainer Docker images and
containers](/linux/step_two).