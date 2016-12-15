# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y agda
    apt-get install -y emacs-nox
    apt-get install -y git
    git clone -b master https://github.com/hazelgrove/agda-popl17.git base-hazelnut
    cd /home/ubuntu/base-hazelnut
    agda all.agda
    cd /home/ubuntu
    git clone -b sums https://github.com/hazelgrove/agda-popl17.git hazelnut-with-sums
    cd /home/ubuntu/hazelnut-with-sums
    agda all.agda
    cd /home/ubuntu
  SHELL
end
