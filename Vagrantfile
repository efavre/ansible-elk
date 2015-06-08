# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|

  config.vm.box = "chef/debian-7.4"
  config.vm.network "forwarded_port", guest: 9200, host: 9201
  config.vm.network "forwarded_port", guest: 5601, host: 5602
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end

end
