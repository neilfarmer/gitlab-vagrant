Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.network "public_network", bridge: "enp39s0", ip: "192.168.0.100"
  config.vm.hostname = "gitlab"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end

  config.vm.provider "virtualbox" do |v|
    v.name = "gitlab"
    v.memory = 4096
    v.cpus = 2
  end
end
