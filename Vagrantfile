# -*- mode: ruby -*-
# vi: set ft=ruby :

# !!! for development only !!!
Vagrant.configure("2") do |config|
  config.vm.hostname = "keanux.vm"

  config.vm.box = "ubuntu/trusty64"
  config.vm.box_url = "ubuntu/trusty64"
  config.vm.provision :shell, path: "tools/vagrant.sh"

  config.vm.synced_folder "./keanux-personal", "/home/vagrant/keanux-personal", create: true

  config.vm.network :private_network, ip: "192.168.33.20"
  config.vm.network :forwarded_port, host:8080, guest:8080

  config.vm.provider "virtualbox" do |v|
    v.gui = false
    v.memory = 1024
    v.cpus = 1
  end
end
