# -*- mode: ruby -*-
# vi: set ft=ruby tabstop=2 :
box_url = "http://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_centos-7.0_chef-provisionerless.box"

Vagrant.configure("2") do |config|
  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.hostname  = "devops-bootcamp.osuosl.org"
  config.vm.box_url   = "#{box_url}"
  config.vm.box = "centos-7"
  config.vm.network "forwarded_port", guest: 8000, host: 8000 
  config.vm.network "forwarded_port", guest: 8080, host: 8080 
  config.vm.network "forwarded_port", guest: 5000, host: 5000 
  config.vm.network "private_network", ip: "55.55.55.5"
  config.vm.provider :virtualbox do |vb|
  config.vm.synced_folder ".", "/myshop", disabled: false 
  # uncomment to enable GUI console
    #vb.gui = "true"
    # uncomment to disable hardware virt
    #vb.customize ["modifyvm", :id, "--hwvirtex", "off"]
    end
end
