% Introduction to Vagrant
% Paul Waring (paul@xk7.net)
% November 16, 2013

# What is VirtualBox?

 - Software for managing virtual machines
 - Basic version is GPL
 - Advanced version has more features and usage restrictions
 - Innotek -> Sun -> Oracle

# What is Vagrant?

 - Wrapper around VirtualBox (and other virtualisation software)
 - Written in Ruby
 - Automatically create, configure and provision virtual machines
 - Open source and free software: MIT Licence (GPL-compatible)
 - www.vagrantup.com

# Why Vagrant?

 - Automatically create and destroy clean, sandboxed environments for development
 - Ensure development matches production: architecture, kernel, packages
 - Ensure all developers in a team are using the same configuration, toolchain etc.
 - Configuration file (Vagrantfile) can be included in project repository

 
# Vagrantfile

 - Plain text configuration file
 - Cascades: system, box, user, project
 - Create a default Vagrantfile: `vagrant init`

# Boxes

 - Containers for base images
 - Saves having to install complete operating system each time
 - Create once by manual installation in VirtualBox, or download examples
 - `vagrant package --base [name] --output [file]`
 - `vagrant box add [name] [url]`
 - `vagrant box add precise32 http://files.vagrantup.com/precise32.box`
 
# Basic Example

 - Create Vagrantfile: `precise-vm/Vagrantfile`
 - Boot VM: `vagrant up`
 - Login: `vagrant ssh`
 - Destroy VM: `vagrant destroy`
 
# Manual Provisioning

 - Boot VM: `vagrant up`
 - Login: `vagrant ssh`
 - Install Nethack: `sudo apt-get install -y nethack-common`
 - Run: `nethack`
 - Destroy VM: `vagrant destroy`
 - Boot VM: `vagrant up`
 - Confirm clean: `which nethack`

# Automatic Provisioning

 - Basic support within Vagrant for this, runs a script after booting
 - More flexibility requires Puppet or Chef
 - Can use built-in provisioning to bootstrap Puppet

# What is Puppet?

 - Configuration management and provisioning
 - Apache 2.0 licence since v2.7, Enterprise platform available
 - Describe desired state of server, Puppet makes it so
 - Declarative vs imperative
 - Vagrant has built-in support for Puppet manifests
 
# Puppet Example

 - Create `manifests/default.pp`
 - Enable Puppet provisioning - one line in Vagrantfile
 - Boot VM as normal: `vagrant up`
 - Run: `nethack`
 - Halt: `vagrant halt`
 - Boot VM, Nethack already installed so no action taken

# Questions

 - Slides and scripts on GitHub under BSD Licence
 - https://github.com/pwaring/vagrant-talk
 - Vagrant: Up and Running, Mitchell Hashimoto (O'Reilly)
