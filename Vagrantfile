# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
    config.ssh.insert_key = false
    config.vm.provider :virtualbox do |provider, override|
        provider.name = "ubuntu-14.04"
        provider.memory = 1024
    end

    config.vm.box = "ubuntu-14.04"
    config.vm.hostname = "sample-app-deploy.dev"
    config.vm.network :public_network, ip: "192.168.34.23"

    config.vm.synced_folder ".", "/vagrant", mount_options: ["dmode=777", "fmode=666"]
end
