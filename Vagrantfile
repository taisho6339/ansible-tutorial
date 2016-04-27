# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.ssh.insert_key = false
    config.vm.provider :virtualbox do |provider, override|
        provider.name = "ansible-tutorial"
        provider.memory = 1024
    end

    config.vm.box = "ubuntu"
    config.vm.hostname = "ansible-tutorial"
    config.vm.network :private_network, ip: "192.168.34.23"

    config.vm.synced_folder ".", "/vagrant", mount_options: ["dmode=777", "fmode=666"]
end
