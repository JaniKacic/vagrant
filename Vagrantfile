# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
	config.vm.box = "ubuntu/bionic64"
	config.vm.network :private_network, ip: "192.168.27.100"
  	config.vm.provider :virtualbox do |vb|
      	vb.memory = 1024
      	vb.cpus = 2 
  	end
  	config.vm.provision :shell, :inline => "apt-get update && apt-get install -y nginx"
  	config.vm.provision :shell, :inline => "ln -s /vagrant /var/www/html/demo"
end
