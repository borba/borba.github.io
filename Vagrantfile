# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/yakkety64"
  config.vm.hostname = "borba-blog"
  config.vm.network "forwarded_port", guest: 4000, host: 4000
  config.ssh.forward_agent = true

  # config.vm.provision "shell", path: "bootstrap.sh", privileged: false

  config.vm.provision "shell", privileged: false, inline: <<-SHELL
    sudo apt-get update
    sudo apt-get -y upgrade
    sudo apt-get -y install libgmp-dev git

    gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
    \\curl -sSL https://get.rvm.io | bash -s stable --ruby=2.3.0
    source ~/.rvm/scripts/rvm

    gem install jekyll bundler
  SHELL
end
