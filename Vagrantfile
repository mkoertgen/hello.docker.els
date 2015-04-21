# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "phusion/ubuntu-14.04-amd64"
  config.vm.network :forwarded_port, guest: 9200, host: 9200
  
  # pull docker image from https://registry.hub.docker.com/u/library/elasticsearch/
  config.vm.provision "docker" do |d|
    d.pull_images "elasticsearch"
    d.run "elasticsearch",
      args: "-p '9200:9200'"
  end  
   
end
