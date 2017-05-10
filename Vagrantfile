# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "pixelpin/ubuntu-1604-rails"
  config.vm.box_url = "file:///T:/pixelpin-ubuntu-1604-rails.box"
  config.vm.network "private_network", ip: "192.168.33.10"
  
  config.vm.provision "shell", inline: <<-SHELL
  
	apt-get update
	apt-get install -y python-dev python-psycopg2 libpq-dev
	cd /vagrant
	sudo python ez_setup.py 
	sudo easy_install pip
	sudo pip install -r requirements.txt
  SHELL
end
