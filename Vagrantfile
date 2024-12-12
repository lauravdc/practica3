# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box_download_insecure=true
  config.vm.box = "daimler/ubuntu-desktop-22.10"
	
  config.vm.network :forwarded_port, guest: 26069, host: 26069, id: "odoopractica3", auto_correct: true
  config.vm.network :forwarded_port, guest: 26432, host: 26432, id: "postgresqlpractica3", auto_correct: true
  config.vm.network :forwarded_port, guest: 26080, host:26080 , id: "pgadminpractica3", auto_correct: true
  config.vm.network :forwarded_port, guest: 26081, host: 26081, id:"mailservicepractica3", auto_correct: true
  config.vm.network :forwarded_port, guest: 26082, host: 26082, id:"pgadminpractica3", auto_correct: true
	
  config.vm.provision "shell", inline: <<-SHELL
    locale-gen es_ES
    locale-gen es_ES.UTF-8
    update-locale LANG=es_ES.UTF-8
    update-locale LANGUAGE=es_ES.UTF-8
    localectl set-x11-keymap es
  SHELL
end
