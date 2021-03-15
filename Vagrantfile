# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "geerlingguy/centos7"

  config.vm.network "forwarded_port", guest: 80, host: 9080

  config.vm.synced_folder "/home/karov/Diplomna", "/vagrant_data"

  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.cpus = 2
    vb.memory = "2048"
  end

  config.vm.provision "ansible" do | ansible | 
    ansible.playbook = "/home/karov/Diplomna/Ansible/Wordpress/playbook.yml"
  end

end
