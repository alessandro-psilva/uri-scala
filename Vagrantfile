# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  
  # mapeando pastas
  config.vm.synced_folder "vagrant_scala", "/vagrant/home/vagrant_scala"
  config.vm.synced_folder "vagrant_provision", "/vagrant/home/vagrant_provision"
  
  # definindo IP
  config.vm.network "private_network", ip: "192.168.1.199"
  
  # definindo configuração para VM
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
	vb.name   = "vagrant-scala"
  end
  
  # provision
  config.vm.provision "shell", inline: <<-SHELL
    bash /vagrant/home/vagrant_provision/vagrant_provision.sh
  SHELL
end
