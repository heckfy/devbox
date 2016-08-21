# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = '2'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'ubuntu/trusty64'

  config.vm.provider :virtualbox do |vb|
    vb.customize ['modifyvm', :id, '--memory', '2048']
  end

  config.vm.network :forwarded_port, guest: 3000, host: 3000

  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'playbook.yml'
  end
end
