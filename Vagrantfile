# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "forwarded_port", guest: 80, host: 80
  config.vm.synced_folder "./shares", "/home/fredyball"
  config.vm.provision  "docker"
  config.vm.provider :virtualbox do |vb|
  vb.customize [ 'modifyvm', :id, '--name', 'distrifinal' ]
  
  end
end  