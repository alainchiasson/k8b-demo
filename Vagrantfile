# -*- mode: ruby -*-
# vi: set ft=ruby :


# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

ANSIBLE_GROUPS = {
              "master" => ["master"],
              "minions" => ["minion1", "minion2", "minion3"],
              "all_groups:children" => ["master", "minions"]
            }

Vagrant.configure("2") do |config|

  config.vm.box = "centos/7"
  config.vm.provider "virtualbox" do | v |
    v.memory = 2048
  end

  # The master node
  config.vm.define "master" do |master|
      master.vm.network "private_network", ip: "192.168.33.10"
      master.vm.hostname = "master"
      master.vm.provision "ansible" do |ansible|
          ansible.playbook = "ansible/playbook-kubtry2.yml"
          ansible.groups = ANSIBLE_GROUPS
      end
  end

  # The master node
  config.vm.define "minion1" do |minion1|
      minion1.vm.network "private_network", ip: "192.168.33.11"
      minion1.vm.hostname = "minion1"
      minion1.vm.provision "ansible" do |ansible|
          ansible.playbook = "ansible/playbook-kubtry2.yml"
          ansible.groups = ANSIBLE_GROUPS
      end
  end

  # The master node
  config.vm.define "minion2" do |minion2|
      minion2.vm.network "private_network", ip: "192.168.33.12"
      minion2.vm.hostname = "minion2"
      minion2.vm.provision "ansible" do |ansible|
          ansible.playbook = "ansible/playbook-kubtry2.yml"
          ansible.groups = ANSIBLE_GROUPS
      end
  end

  # The master node
  config.vm.define "minion3" do |minion3|
      minion3.vm.network "private_network", ip: "192.168.33.13"
      minion3.vm.hostname = "minion3"
      minion3.vm.provision "ansible" do |ansible|
          ansible.playbook = "ansible/playbook-kubtry2.yml"
          ansible.groups = ANSIBLE_GROUPS
      end
  end


end
