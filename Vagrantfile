# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "santicashe0920/PARCIAL1"
  config.vm.box_version = "0.0.1"
end
Vagrant.configure("2") do |config|
 if Vagrant.has_plugin? "vagrant-vbguest"
 config.vbguest.no_install = true
 config.vbguest.auto_update = false
 config.vbguest.no_remote = true
 end
 config.vm.define :cliente do |cliente|
 cliente.vm.box = "centos/stream8"
 cliente.vm.network :private_network, ip: "192.168.50.2"
 cliente.vm.hostname = "cliente"
 cliente.vm.synced_folder ".", "/vagrant", type: "rsync" 
 end
 config.vm.define :servidor do |servidor|
 servidor.vm.box = "centos/stream8"
 servidor.vm.network :private_network, ip: "192.168.50.3"
 servidor.vm.hostname = "servidor"
 servidor.vm.synced_folder ".", "/vagrant", type: "rsync" 
 end
end
