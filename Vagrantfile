# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/vivid64"
  config.vm.hostname = "weavedev"
  config.ssh.insert_key = false
  config.vm.network "private_network", type: "dhcp"

  config.vm.provider :virtualbox do |v|
    # Setting VM name and increasing RAM size
    v.customize [
      "modifyvm", :id,
      "--memory", "2048"
    ]

  end

  config.vm.provision "ansible" do |a|
    a.playbook = "playbook.yml"
    # Run commands as root.
    a.sudo = true
  end

end

