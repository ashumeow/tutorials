+++
title = "Install Docker for Wiindows"
description = "Getting started with Docker"
keywords = ["install, demo, Docker, windows"]
[menu.windows]
identifier = "windows_install"
weight = 1
+++

# Install Docker for Windows

Because Docker relies on Linux-specific features, you can't run Docker natively
in Windows. Instead, you must install the Boot2Docker application. The
application installs a VirtualBox Virtual Machine (VM), Docker itself, and the
Boot2Docker management tool. These three things allow you to run Docker on
Windows.

## Step 1: Check your version

Your machine must be running Windows 7.1, 8/8.1 or newer to run Boot2Docker. 
To find out what version of Windows you have:

1. Right click the windows message and choose **System*. 

    ![Which version](/windows/images/win_ver.png)
    
    If you aren't using a supported version, you could consider upgrading your
    operating system.

2. Make sure your Windows system supports Hardware Virtualization Technology and that virtualization is enabled.

    #### For Windows 8 or 8.1

	  Choose **Start > Task Manager** and navigate to the **Performance** tab.          
	  Under **CPU** you should see the following:

      ![Release page](/windows/images/virtualization.png)
    
    If virtualization is not enabled on your system, follow the manufacturer's instructions for enabling it.
    
    ### For Windows 7 
    
	  Run the <a href="http://www.microsoft.com/en-us/download/details.aspx?id=592"
target="_blank"> Microsoft® Hardware-Assisted Virtualization Detection Tool</a> 
and follow the on-screen instructions.


## Step 2: Install Boot2Docker

In this section, you install the Boot2Docker software and several "helper" applications. The installation adds the following software to your machine:

* Docker Client for Windows
* Boot2Docker management tool and ISO
* Oracle VM VirtualBox 
* Git MSYS-git UNIX tools

If you have a previous version of VirtualBox installed, do not reinstall it with the Boot2Docker installer. When prompted, uncheck it.

1. Click <a href="https://github.com/boot2docker/windows-installer/releases/download/v1.6.2/docker-install.exe" >to download the Boot2Docker for Windows installer</a>.
   
	  The browser downloads the installer to your machine. It can take about a
    minute.

3. Open the downloaded `docker-install.exe` file from your browser or by double-click the file itself.
    
    If Windows security dialog prompts you to allow the program to make a
    change, choose **Yes**. The system displays the **Setup - Boot2Docker for
    Windows** wizard.
   
      ![Release page](/windows/images/installer_open.png)

4. Press **Next** to accept all the defaults and then **Install**.

	  Accept all the installer defaults. The installer takes a few minutes to install all the components:
	  
	   ![Release page](/windows/images/win_installing.png)
        
5.  When notified by Windows Security the installer will make changes, make sure you allow the installer to make the necessary changes.
    
    When it completes, the installer reports it was successful:
    
    ![Success](/windows/images/finish.png)
    
6. Press **Finish**.


## Step 3. Verify your installation

The installer places Boot2Docker and VirtualBox in your **Applications** folder.
In this step, you start Boot2Docker and run a simple Docker command.

1. On your Desktop, find the Boot2Docker icon.

    ![Desktop](/windows/images/icon-set.png)
    
2. Click the icon to launch a Boot2Docker terminal.

    If the system displays a **User Account Control** prompt to allow VirtualBox to make changes to your computer. Choose **Yes**.

    The terminal does several things to set up Boot2Docker for you. When it is done, the terminal displays the `$` prompt.
    
     ![Desktop](/windows/images/b2d_shell.png)
     
    The terminal runs a special `bash` environment instead of the standard Windows command prompt. The `bash` environment is required by Docker.

3.  Make the terminal active by click your mouse next to the `$` prompt.

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

At this point, you have successfully installed Docker. Leave the Boot2Docker
window open. Go to the next page to [read a very short introduction to Docker
images and containers](/windows/step_two).
