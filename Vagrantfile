# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.provision :shell, :path => "provisioning/git.sh"
  config.vm.provision :shell, :path => "provisioning/erlang.sh"
  config.vm.provision :shell, :path => "provisioning/elixir.sh"

  config.vm.network "forwarded_port", guest: 9091, host: 9091
  config.vm.network "forwarded_port", guest: 9092, host: 9092

end
