Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.network "public_network"
  config.vm.synced_folder "app/", "/var/www/html"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "Vagrant-Ubuntu"
    vb.memory = 1024
    vb.cpus = 01
  end
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y apache2
  SHELL
end
