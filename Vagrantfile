VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.ssh.insert_key = false
  config.vm.provider :virtualbox do |v|
    v.memory = 512
    v.linked_clone = true
  end

  # Application server 1.
  config.vm.define "inventory1" do |inventory|
    inventory.vm.hostname = "inventory1.test"
    inventory.vm.box = "geerlingguy/ubuntu2004"
    inventory.vm.network :private_network, ip: "192.168.28.71"
  end

  # Application server 2.
  config.vm.define "inventory2" do |inventory|
    inventory.vm.hostname = "inventory2.test"
    inventory.vm.box = "geerlingguy/ubuntu2004"
    inventory.vm.network :private_network, ip: "192.168.28.72"
  end
end