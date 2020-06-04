# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = 'bento/ubuntu-19.10'

  config.vm.provider "virtualbox" do |vb|
    vb.name = 'quarantine'

    require 'etc'
    num_cpus = Etc.nprocessors
    vb.cpus = ENV.fetch('LINUX_PLAYGROUND_CPUS', num_cpus)

    vb.memory = ENV.fetch('LINUX_PLAYGROUND_MEMORY', 2048)
  end

  config.vm.provision "shell", inline: "apt-get update && apt-get install -y python-dev"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
