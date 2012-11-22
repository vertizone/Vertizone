# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.define :master do |master_config|
    master_config.vm.box = "master"
    master_config.vm.forward_port 80, 8080
    master_config.vm.network :hostonly, "10.10.10.51"
  end

  config.vm.define :slave do |slave_config|
    slave_config.vm.box = "slave"
    slave_config.vm.forward_port 90, 9090
    slave_config.vm.network :hostonly, "10.10.10.52"
  end
end