# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "master1" do |config|
    config.vm.box = "ubuntu/focal64" # 20.04 LTS 버전의 박스명
    config.vm.provider "virtualbox" do |vb|
      vb.name = "master1" # 인스턴스 이름을 설정한다 (master)
      vb.cpus = 2
      vb.memory = 3072
    end
    config.vm.hostname = "master1"
    config.vm.network "private_network", ip: "192.168.56.30"
    config.disksize.size = "30GB"
  end

  config.vm.define "web1" do |config|
    config.vm.box = "ubuntu/focal64"
    config.vm.provider "virtualbox" do |vb|
      vb.name = "web1"
      vb.cpus = 2
      vb.memory = 3072
    end
    config.vm.hostname = "web1"
    config.vm.network "private_network", ip: "192.168.56.31"
    config.disksize.size = "30GB"
  end

  config.vm.define "db1" do |config|
    config.vm.box = "ubuntu/focal64"
    config.vm.provider "virtualbox" do |vb|
      vb.name = "db1"
      vb.cpus = 2
      vb.memory = 3072
    end
    config.vm.hostname = "db1"
    config.vm.network "private_network", ip: "192.168.56.33"
    config.disksize.size = "30GB"
  end


  # Hostmanager plugin
  config.hostmanager.enabled = true
  config.hostmanager.manage_guest = true

  # Enable SSH Password Authentication
  config.vm.provision "shell", inline: <<-SHELL
    sed -i 's/ChallengeResponseAuthentication no/ChallengeResponseAuthentication yes/g' /etc/ssh/sshd_config
    sed -i 's/archive.ubuntu.com/ftp.daum.net/g' /etc/apt/sources.list
    sed -i 's/security.ubuntu.com/ftp.daum.net/g' /etc/apt/sources.list
    systemctl restart ssh
  SHELL
end