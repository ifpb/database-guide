# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "forwarded_port", guest: 3306, host: 3306
  config.vm.provider "virtualbox" do |vb|
    vb.name = "MySQL VM"
  end
  config.vm.provision "shell", path: "install/mysqlserver.sh"
end
