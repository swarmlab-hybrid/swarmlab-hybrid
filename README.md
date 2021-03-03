<img align="right" width="300" height="300" src="https://git.swarmlab.io:3000/zeus/swarmlab-hybrid/raw/branch/master/docs/images/hybrid-1.png">

# Swarmlab Hybrid
  

#### **Welcome to Swarmlab.io**

##### **On demand Labrooms**
##### **Ready-to-Use Virtual Labs one click away.**
  
  
 
### Table of contents
  
1. [Features](#introduction)
2. [System requirements ](#systemrequirements)
3. [Prerequisites](#prerequisites)
4. [Installation](#installation)
5. [More info](#moreinfo)


### <a name="introduction"></a>
## <b>Swarmlab Hybrid</b> is Swarmlabs younger, more tech savvy brother.  

Swarmlab hybrid provides the user with the unique abillity to create  Labrooms (or other applications) and share them as project images expanding the simple swarmlab Labrooms to full-blown systems. An all of that <b>using onlly the browser and the command line</b> of their system.
  
## Why?
Ever imagined having a normal lesson as you would in the University from the comfort of your livingroom?  
Ever created a service that you would like to test on a real-world network?  
Ever designed an Labroom/application you would like to distribute to your students/applications?  
Swarmlab Hybrid comes to bridge the gap between tutor and student, the coder/developer of a service and the and user and at the same time meet the needs for a real-world testing environment.   
With Hybrid we can now as part of the cloud work <b>independantly</b> but also stay <b>connected</b>.  
The hybrid format allows us to utilize the power of Swarmlab itself but also combine it with the practiaclly unlimited computing of our own machines.

## How?
How does Swarmlab Hybrid differ from Swarmlab? Well...its Swarmlab...just....HYBRID!  
Easy enough right? But what does that mean in practice?  
Well for us it means a couple million more lines of code. For you it means a few more installation steps and the newfound access to YOUR OWN RESOURCES!

You will be connected to the Swarmlab Cloud (hence HYBRID) but you will be able to use your own storage(move files around, delete/copy etc),your own networking and computational power(cpu/graphics etc) and create a system exactly the way you need it.  

This way you will be able to :
- <b>create</b> images for testing.  
- <b>Run</b> them using docker.  
- <b>Share</b> them for others to use and develop.  
- Finally <b>browse the cloud</b> for shared images to <b>integrate</b> into your project and make it even better.  

## Ready to run out-of-the-box

Normally the docker dataflow is as described in the following images:

<img align="center"  src="https://git.swarmlab.io:3000/zeus/swarmlab-hybrid/raw/branch/master/docs/images/docker-build.png">
<img align="center"  src="https://git.swarmlab.io:3000/zeus/swarmlab-hybrid/raw/branch/master/docs/images/docker-run.png">

To make the service easier to use we have created an ever-growing database of readilly accessible images you can choose from, thus making the first step optionall!

## Swarmlab vs Swarmlab Hybrid in a nutshell

### Swarmlab

- Ready to use, on demand virtual labs
- Optimized for both Students and Tutors
- Tutors bootstrap their labrooms using our tools

- Students can:  
 - join the created labrooms according to their interrests
 - run the evailable labs at will
 - create their own rooms for exercising  


### Hybrid
- Create Labrooms/Applications
- Run and manage said rooms and application
- create once - scale up or down without rebuilding
- Connect multiple computers through a network.
- Move Labs between environments
- Create your own labs 
- open source barebone -> <b>Share them with your friends</b>


## IMPORTANT
:exclamation: If you wish to use the service in Hybrid mode, that is if you want to share, download or perform other activites on the cloud you will need a <b>KEY</b>. Read installation instructions to learn how to do that.  

Local usage of the service <b>doesnt</b> require one, you only need to log in to your account.  

## System requirements<a name="systemrequirements"></a>
  
  
**Before** you create and configure a hybrid deployment using the swarmlab-agent client, your Local Machines need to meet certain requirements.
  

> If you don't meet those requirements, you won't be able to complete the steps within the swarmlab-agent client and you won't be able to configure a hybrid deployment between your Local Enviroment and Swarmlab Online Enviroment.
   

- A Linux Server (Virtual or Physical) 	
 - You must have super user privileges (root/sudo)
- Docker Engine- Community version 18 or later is required. 	
 -  Docker Engine is supported on x86_64 (or amd64), armhf, and arm64 architectures.
- RAM
 - Absolute minimum to run the daemon and some very light containers - 512MB
 - Minimum for “comfortable” usage – 2GB
- CPU
 - Minimum: 2
 - Recommended 4+
- Disk Space
 - 10 GB for internal requirements.
 - The amount of additional disk space soloemnly depends on you intended use.

:warning: Since Docker uses hypervisor the host NEEDS TO HAVE VIRTUALIZATION ENABLED!




## Prerequisites<a name="prerequisites"></a>

* node version >15

  ```sh
  curl -sL https://deb.nodesource.com/setup_15.x | sudo -E bash -
  sudo apt-get install -y nodejs
  ```
* docker 

  ```sh
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
  sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
  sudo apt update
  sudo apt install -y docker-ce
  sudo usermod -aG docker [USERNAME]
  ```
* docker-compose

  ```sh
  sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
  sudo chmod +x /usr/local/bin/docker-compose
  sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
  ```
* pm2

  ```sh
  sudo npm install -g pm2
  ```
* wireguard

  ```sh
  sudo apt install wireguard jq
  ```

## Installation<a name="installation"></a>
  
### for *nix
  
<br />
<p align="center">
  <p align="center">
- Clone the repo

   ```sh
   git clone --recurse-submodules https://git.swarmlab.io:3000/zeus/swarmlab-hybrid.git
   ```
- Install it!

   ```sh
   cd swarmlab-hybrid
   ./install.sh
   ```
- Open URL __http://localhost:3088__ in browser 
 - Get a Swarmlab account. 
- Get a free API Key at  **Settings->Enable the Swarmlab hybrid** Menu
  </p>
</p>

### for windows
You can find ready to run VM images <a href="https://uniwagr-my.sharepoint.com/:u:/g/personal/ice19390012_uniwa_gr/EbhjQIeiDeNFkfkSBWczRggBcJq2Pv6lAJs-NKkT4hXg-g?e=0VC0xa">here</a>.

### More Info<a name="moreinfo"></a>

You can find our docs in **docs** Directory

The Swarmlab docs are in **AsciiDoc** (similar to markdown), **PDF** and **html** format

  
For real-time rendering in browser Asciidoc an add-on can be found here:

http://docs.swarmlab.io/SwarmLab-HowTos/labs/Howtos/doclive/asciidoc.adoc.html#_setup_live_preview_using_a_web_browser

