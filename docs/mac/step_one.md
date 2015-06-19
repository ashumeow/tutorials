+++
title = "Install Docker on OS X"
description = "Getting started with Docker"
keywords = ["install, demo, Docker, OS X"]
[menu.mac]
identifier = "mac_install"
weight = 1
+++

# Install Docker Mac OS X

Because Docker relies on Linux-specific features, you can't run Docker natively
in OS X. Instead, you must install the Boot2Docker application. The application
installs a VirtualBox Virtual Machine (VM), Docker itself, and the Boot2Docker
management tool. These three things allow you to run Docker on Mac OS X.

## Step 1: Check your version

Your Mac must be running OS X 10.6 "Snow Leopard" or newer to run Boot2Docker.
To find out what version of the OS you have:

1. Choose **About this Mac** from the Apple menu. 

    ![Which version](/mac/images/which_version.png)

    The version number appears directly below the words `OS X`.

2. If you have the correct version, go to the next step.

    If you aren't using a supported version, you could consider upgrading your
    operating system.


## Step 2: Install Boot2Docker

1. Click <a href="https://github.com/boot2docker/osx-installer/releases/download/v1.6.2/Boot2Docker-1.6.2.pkg" >to download the Boot2Docker installer</a>.
   
	  The browser downloads the package to your machine. It can take about a
    minute.

3. Open the downloaded package file.

    You can open it from your browser or by double-click the file itself. When you open the package, the system displays the **Install Boot2Docker for
    Mac OS X** wizard.
    
    ![Package installer](/mac/images/package_installer.png)

4. Press **Continue** and then **Install**.

	  Accept all the installer defaults. Your system might warn you about the
   installer.  
    
    ![Installer](/mac/images/install_software.png)
    
5.  If prompted, provide your **Username**, **Password**, and press **Install Software**.
    
    When it completes, the installer reports it was successful:
    
    ![Success](/mac/images/successful.png)
    
6. Press **Close**.


## Step 4. Verify your installation

The installer places Boot2Docker and VirtualBox in your **Applications** folder.
In this step, you start Boot2Docker and run a simple Docker command.

1. Open the **Launchpad** and locate the Boot2Docker icon.

    ![Launchpad](/mac/images/applications_folder.png)
    
2. Click the icon to launch a Boot2Docker terminal.

    The terminal does a number of things to set up Boot2Docker for you. When it
    is done setting up, it runs the `docker version` command.
    
        $ $(/usr/local/bin/boot2docker shellinit)
        Writing /Users/mary/.boot2docker/certs/boot2docker-vm/ca.pem
        Writing /Users/mary/.boot2docker/certs/boot2docker-vm/cert.pem
        Writing /Users/mary/.boot2docker/certs/boot2docker-vm/key.pem

        $ docker version
        Client version: 1.6.2
        Client API version: 1.18
        Go version (client): go1.4.2
        Git commit (client): 7c8fca2
        OS/Arch (client): darwin/amd64
        Server version: 1.6.0
        Server API version: 1.18
        Go version (server): go1.4.2
        Git commit (server): 4749651
        OS/Arch (server): linux/amd64
        bash: prompt_git: command not found

3.  Click your mouse in the terminal window to make it active.

    If you aren't familiar with a terminal window, here are some quick tips. 
    
    ![Teriminal](/img/terminal.png) 
    
    The prompt is traditionally a `$` dollar sign. You type commands into the
    *command line* which is the area after the prompt. Your cursor is indicated
    by a highlighted area or a `|` that appears in the command line. After
    typing a command, always press RETURN.

4. Type the `docker run hello-world` commmand and press RETURN.

    The command does some work for you, if everything runs well, the command's
    output looks like this:
    
        $ docker run hello-world
        Unable to find image 'hello-world:latest' locally
        Pulling repository hello-world
        91c95931e552: Download complete 
        a8219747be10: Download complete 
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

At this point, you have successfully installed Docker. Leave the Boot2Docker window open. Now, go to the next page to [read a very short introduction Docker images and containers](/mac/step_two).
