# -*- mode: ruby -*-
# vi: set ft=ruby :
$bootstrap=<<-SCRIPT
apt-get update
apt-get install -y ca-certificates curl gnupg2 lsb-release
curl -fsSL https://download.docker.com/linux/debian/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian \
  $(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
apt-get update
apt-get install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin
usermod -aG docker vagrant
service docker restart
SCRIPT

Vagrant.configure("2") do |config|
  config.vm.box = "debian/bullseye64"

  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provider "libvirt" do |vb|
    vb.memory = "3072"
    vb.cpus = 2
  end
  config.vm.provision "shell", inline: $bootstrap
  config.vm.synced_folder ".", "/vagrant", disabled: true

end
