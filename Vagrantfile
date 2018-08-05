# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|

  config.vm.define 'vagrant1' do |v|
    v.vm.box = 'ubuntu/trusty64'
    v.vm.boot_timeout = 400
    v.vm.network 'private_network', ip: '192.168.33.20'
    v.vm.network 'forwarded_port', guest: 22, host: 2222, id: "ssh"
    v.vm.provider 'virtualbox' do |vb|
      vb.name = 'Vagrant Ansible 1'
      vb.memory = "1024"
    end
  end

  config.vm.define 'vagrant2' do |v|
    v.vm.box = 'ubuntu/trusty64'
    v.vm.network 'private_network', ip: '192.168.33.21'
    v.vm.network 'forwarded_port', guest: 22, host: 2200, id: "ssh"
    v.vm.provider 'virtualbox' do |vb|
      vb.name = 'Vagrant Ansible 2'
      vb.memory = "1024"
    end
  end
  
end
