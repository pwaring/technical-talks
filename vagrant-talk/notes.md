% Introduction to Vagrant
% Paul Waring
% November 16, 2013

## Examples

Examples to run through during the course of the slides.

### Creating a box

First produce VM image manually in VirtualBox.

````
vagrant package --base wheezy32 --output wheezy32.box
````

### Install Puppet

Add the following line to `Vagrantfile`:

````
  config.vm.provision "shell", path: "provision.sh"
````

### Configure Puppet

