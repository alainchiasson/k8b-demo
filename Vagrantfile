# -*- mode: ruby -*-
# vi: set ft=ruby :


# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

ANSIBLE_GROUPS = {
              "master" => ["node1"],
              "minions" => ["node2", "node3", "node4"],
              "all_groups:children" => ["master", "minions"]
            }

Vagrant.configure("2") do |config|

  config.vm.box = "centos/7"
  config.vm.provider "virtualbox" do | v |
    v.memory = 2048
  end

  # The master node
  config.vm.define "node1" do |node1|
      node1.vm.network "private_network", ip: "192.168.33.10"
      node1.vm.hostname = "node1"
      node1.vm.provision "ansible" do |ansible|
          ansible.playbook = "ansible/playbook.yml"
          ansible.groups = ANSIBLE_GROUPS
      end
  end

  # The master node
  config.vm.define "node2" do |node2|
      node2.vm.network "private_network", ip: "192.168.33.11"
      node2.vm.hostname = "node2"
      node2.vm.provision "ansible" do |ansible|
          ansible.playbook = "ansible/playbook.yml"
          ansible.groups = ANSIBLE_GROUPS
      end
  end

  # The master node
  config.vm.define "node3" do |node3|
      node3.vm.network "private_network", ip: "192.168.33.12"
      node3.vm.hostname = "node3"
      node3.vm.provision "ansible" do |ansible|
          ansible.playbook = "ansible/playbook.yml"
          ansible.groups = ANSIBLE_GROUPS
      end
  end

end