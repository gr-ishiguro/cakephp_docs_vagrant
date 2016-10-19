# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vbguest.auto_update = false

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "CentOS65"

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = "http://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_centos-6.8_chef-provisionerless.box"

  # Share an additional folder to the guest VM.
  config.vm.synced_folder "/path/to/your/cakephp/docs", "/forked_docs"
  config.vm.synced_folder "vagrant_setups", "/vagrant_setups"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  config.vm.provider :virtualbox do |vb|
    # Don't boot with headless mode
    vb.gui = false

    # Use VBoxManage to customize the VM. For example to change memory:
    vb.customize ["modifyvm", :id, "--memory", "1024"]
  end

  config.vm.boot_timeout = 120

  config.vm.provision "shell", inline: "/bin/bash /vagrant_setups/vagrant_setup.sh"
end
