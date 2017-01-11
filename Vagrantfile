# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "ubuntu/xenial64"

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  # config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"

  # Application Server
  config.vm.define "app" do |app|
    app.vm.hostname = "bika"
    app.vm.box = "ubuntu/xenial64"
    app.vm.provision "shell", inline: "apt-get install -y python aptitude"
    app.vm.network :private_network, ip: "192.168.33.10"

    # sentry.vm.box_url = "http://files.vagrantup.com/trusty64.box"
    # app.vm.provider "virtualbox" do |provider|
    #   provider.customize ["modifyvm", :id, "--memory", "2048"]
    #   provider.customize ["modifyvm", :id, "--cpus", "1"]
    # end

    # app.vm.provision "ansible" do |ansible| 
    #   ansible.playbook = "bika.yml"
    #   ansible.verbose = 'vvv'
    # end 
  end

end
