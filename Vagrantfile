# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.hostname = "node.local"

  config.vm.box = "precise32"
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"

  config.vm.network :private_network, ip: "10.10.10.10"

  config.vm.synced_folder "../", "/home/vagrant/workspace"

  config.vm.provision :shell, :path => "upgrade-puppet.sh"

  config.vm.provision :puppet do |puppet|
     puppet.manifests_path = "manifests"
     puppet.manifest_file  = "init.pp"
     puppet.module_path    = "modules"
     puppet.options        = "--hiera_config /vagrant/hiera.yaml"
  end
end
