# -*- mode: ruby -*-
# vi: set ft=ruby :

# Freeciv-web Vagrant Vagrantfile - play.freeciv.org 
# 2014-02-17 - Andreas R�sdal
#
# Run 'vagrant up' in this directory, which will create a VirtualBox image,
# and run scripts/freeciv-web-bootstrap.sh to install Freeciv-web for you.
# Then point your browser to localhost:8080/
#

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "ubuntu64"

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/saucy/current/saucy-server-cloudimg-amd64-vagrant-disk1.box"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  config.vm.network :forwarded_port, guest: 80, host: 80

 
   config.vm.provider "virtualbox" do |v|
    v.memory = 6000
   end

  # run the Freeciv bootstrap script on startup
  config.vm.provision :shell, :path => "scripts/freeciv-web-bootstrap.sh"


end
