Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.provision :shell, path: "provision.sh"
  config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'"
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
  end
  config.vm.synced_folder ".\\src", "/home/vagrant/src"
  config.vm.network "private_network", ip: "192.168.23.33"
  config.vm.network "forwarded_port", guest: 8085, host: 8085

end
