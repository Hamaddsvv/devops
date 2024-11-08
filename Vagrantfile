Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-22.04"
  config.vm.box_download_options = { "ssl-no-revoke" => true }
  
  config.vm.network "private_network", ip: "192.167.33.10"
  config.vm.network "public_network"
  config.vm.network "forwarded_port", guest: 80, host: 8081
  
  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = "8000"
    vb.cpus = "2"
  end
  
  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get upgrade -y
    sudo apt-get install -y apache2
    sudo apt-get install -y openjdk-11-jdk
    wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
    sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
    sudo apt-get update
    sudo apt-get install -y jenkins
    sudo systemctl start jenkins
    sudo systemctl enable jenkins
  SHELL
end
