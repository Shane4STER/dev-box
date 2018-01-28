Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-17.10"

  config.vm.provider "virtualbox" do |v|
    v.gui = false
    v.memory = 2048
    v.cpus = 2
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
