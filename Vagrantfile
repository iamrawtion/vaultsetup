# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: "echo Hello"

  $num_instances = 1
  (1..$num_instances).each do |i|
    config.vm.define "agent#{i}" do |agent|
      agent.vm.box = "ubuntu/trusty64"
      agent.vm.box_url = "ubuntu/trusty64"
      agent.vm.network :private_network, ip: "192.168.3.#{i+150}"
      agent.vm.hostname = "agent#{i}"
      agent.vm.provider :virtualbox do |v|
        v.memory = "512"
        v.cpus = 1
        v.name = "agent#{i}"
      end
    end
  end

end
