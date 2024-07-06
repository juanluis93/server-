Vagrant.configure("2") do |config|
    config.vm.define "web1" do |web1|
      web1.vm.box = "ubuntu/bionic64"
      web1.vm.network "private_network", type: "dhcp"
      web1.vm.provision "shell", inline: <<-SHELL
        apt-get update
        apt-get install -y apache2
        mkdir -p /var/www/html
      SHELL
      web1.vm.synced_folder ".", "/var/www/html"
    end
  
    config.vm.define "web2" do |web2|
      web2.vm.box = "ubuntu/bionic64"
      web2.vm.network "private_network", type: "dhcp"
      web2.vm.provision "shell", inline: <<-SHELL
        apt-get update
        apt-get install -y apache2
        mkdir -p /var/www/html
      SHELL
      web2.vm.synced_folder ".", "/var/www/html"
    end
  end
  