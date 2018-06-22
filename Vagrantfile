Vagrant.configure("2") do |config|
  config.vm.box = "archlinux/archlinux"

  ENV['LC_ALL']="en_US.UTF-8"
  ENV['LC_CTYPE']="en_US.UTF-8"
  ENV['LANG']="en_US.UTF-8"

  config.vm.provider "virtualbox" do |v|
    v.gui = false
    v.memory = 2048
    v.cpus = 2
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.extra_vars = "variables.json"
    ansible.playbook = "playbook.yml"
  end
end
