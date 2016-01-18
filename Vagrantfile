Vagrant.configure(2) do |config|

  #
  # Run Ansible from the Vagrant Host
  #

  config.vm.define "ubuntu" do |ubuntu|
    ubuntu.vm.box = "ubuntu/trusty64"
    ubuntu.vm.hostname = "ubuntu"
    ubuntu.vm.synced_folder ".", "/vagrant"
    ubuntu.vm.network "private_network", ip: "192.168.90.10"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "tasks/main.yml"
  end

end
