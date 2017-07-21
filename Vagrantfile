# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"
ANSIBLE_DEBIAN           = <<ANSIBLE
  sudo echo 'deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main' >> /etc/apt/sources.list
  sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 93C4A3FD7BB9C367
  sudo apt-get -y update && apt-get install -y ansible
ANSIBLE

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  
  # Debian
  config.vm.define "debian_ansible" do |debian|
    debian.vm.hostname = "debian.lab"
    debian.vm.box      = "debian/jessie64"
    debian.vm.network "private_network", ip: "192.168.200.10"

    debian.vm.provider "virtualbox" do |v|
      v.gui    = true
      v.name   = "Debian Jessie - Ansible"
      v.memory = 1024
      v.cpus   = 2
    end

    debian.vm.provision "shell", inline: ANSIBLE_DEBIAN
 
  end

end
