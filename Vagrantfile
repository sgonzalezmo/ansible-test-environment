# Number of ansible slave nodes
NODES = 1

Vagrant.configure(2) do |config|
  # Specifying the box we wish to use
  config.vm.box = "centos/7"

  config.vm.define "ansible-master" do |config|
    config.vm.provider "virtualbox" do |vb|
      vb.name = "ansible_master"
    end
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/ansible-master.yml"
    end
    config.vm.hostname = "ansiblemaster"
    config.vm.network :private_network, ip: "10.0.0.10"
  end

  (1..NODES).each do |i|
      config.vm.define "ansible-node#{i}" do |config|
        config.vm.provider "virtualbox" do |vb|
          vb.name = "ansible_node#{i}"
        end
        config.vm.hostname = "ansiblenode#{i}"
        config.vm.network :private_network, ip: "10.0.0.#{i + 10}"
      end
    end
end