# packer-redis64

firedot-redis64

**This repository is based on [that](https://github.com/nabels-coolblue/packer-xenial64) repository.**

Here you could find instructuions how to create a basic Vagrant box with Packer. 

**The box will also have redis-server installed.**

You could learn more about Vagrant [here](https://www.vagrantup.com/intro/index.html)

## Used technologies

**Packer** 
You could learn more about packer by visiting: https://www.packer.io/intro/

**VirtualBox** 
You could learn more about VirtualBox by visiting: https://www.virtualbox.org/

### VirtualBox phase
Install VirtualBox on your machine. 
Instructions on how it's done may be found [here](https://www.virtualbox.org/manual/ch02.html)

### Packer phase
1. Download and install [packer](https://www.packer.io/downloads.html) 
2. Run the following command in the directory where you have cloned the repository:

````
packer build template.json
````
3. You could upload the box created by you during the packer phase to the [VagrantCloud](https://app.vagrantup.com/boxes/search) 
# kitchen-redis64
Kitchen-vagrant test for Vagrant box

##Prerequisites: 
* [VirtualBox](https://www.virtualbox.org/manual/ch02.html)
* [Vagrant](https://www.vagrantup.com/downloads.html)

**This repository contains instructions how to perform
kitchen-vagrant test on the box built from this repository: 
[git](git@github.com:firedot/packer-redis64.git)**

1. Follow the instructions from the repository quoted above. 
2. Once the process is completed, run the following command: 
````
vagrant box add --name redis64 redis64.box
````
** This will make the box created with packer available to vagrant**
    2.1 Another way to obtain the box is by executing the following command: 
    ````
    vagrant box add firedot/redis64
    ````
    The previous line will download the already built box from the VagrantCloud. 
3. Install kitchen by installing the [ChefDK](https://downloads.chef.io/chefdk)
4. Go into the directory where you cloned this repository

