Vagrant.configure("2") do |configuration|

  configuration.vm.box = "ubuntu/trusty64"
  configuration.vm.synced_folder "./", "/home/vagrant/site",
    create: true,
    id: "vagrant-site"
  configuration.vm.provision :shell,
    path: "provision/provision-jekyll.sh"
  configuration.vm.network "private_network", ip: "192.168.0.100"
  configuration.vm.network "forwarded_port",
    guest: 4000,
    host: 8080

end
