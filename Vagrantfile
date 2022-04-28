Vagrant.configure("2") do |config|
  config.vm.box = "generic/centos8"
  config.vm.provision :shell, path: "bootstrap.sh"
  config.vm.synced_folder ".", "/vagrant"
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "forwarded_port", guest: 3000, host: 3000

  config.vm.provision "ansible_local" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "playbook.yml"
  end
end