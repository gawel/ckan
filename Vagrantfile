# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  config.cache.auto_detect = true
  config.vm.network :private_network, ip: "192.168.42.42"
  config.vm.network :forwarded_port, guest: 80, host: 8080
  config.ssh.forward_agent = true
   config.vm.provision "shell",
    path: "bin/travis-install-dependencies"
end
