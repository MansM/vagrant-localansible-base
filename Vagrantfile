Vagrant.configure(2) do |config|
  VROOT=""
  config.ssh.insert_key = false

  config.vm.box = "mansm/CentOS-7"
  
  config.vm.provider "virtualbox" do |v|
    v.linked_clone = true
  end


  config.vm.define "manager1" do |vmconfig|
    vmconfig.vm.hostname = "manager1"
    vmconfig.vm.network "private_network", ip: "172.16.55.11"
    vmconfig.vm.provision "shell", inline: "yum install -y epel-release && yum install -y ansible"
    vmconfig.vm.provision "ansible_local" do |ansible|
      ansible.playbook =  "ansible/playbook.yml"
      ansible.sudo = true
      ansible.verbose = "v"
    end
  end
end