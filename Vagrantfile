# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  def configure(c, addr)
    c.vm.box = "bento/ubuntu-16.04"
    c.vm.network :private_network, ip: addr
    c.vm.box_check_update = false
    c.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    end
  end

  config.vm.define "vitess1" do |c|
    configure c, "192.168.50.11"
  end
  config.vm.define "vitess2" do |c|
    configure c, "192.168.50.12"
  end
  config.vm.define "vitess3" do |c|
    configure c, "192.168.50.13"
  end
end
