# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.hostname = "elixdev"
  config.vm.network :forwarded_port, guest: 5080, host: 5080, auto_correct: true

  # change this to your needs
  config.vm.synced_folder "..", "/home/ubuntu/work"

  config.vm.provider :virtualbox do |v|
    # Setting VM name and increasing RAM size
    v.customize [
      "modifyvm", :id,
      "--memory", "4096"
    ]

    # without this symlinks can't be created on the shared folder
    v.customize [
      "setextradata", :id,
      "VBoxInternal2/SharedFoldersEnableSymlinksCreate/v-root", "1"
    ]

  end

  config.vm.provision "ansible_local" do |a|
    a.playbook = "playbook.yml"
    # Run commands as root.
    a.sudo = true
  end

end

