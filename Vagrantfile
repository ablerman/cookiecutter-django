# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "ubuntu/trusty64"
    config.vm.provider :virtualbox do |vb|
        vb.customize ["modifyvm", :id, "--memory", "1024"]
    end

    config.vm.network "private_network", ip: "192.168.50.6"
    config.vm.synced_folder "./", "/{{cookiecutter.repo_name}}", type: "nfs", mount_options:['actimeo=1']
    config.vm.network :forwarded_port, guest: 8000, host: 10000
end
