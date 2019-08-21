# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANT_API_VERSION=2

Vagrant.configure(VAGRANT_API_VERSION) do |config|
  config.ssh.username = "IEUser"
  config.ssh.password = "Passw0rd!"
  config.ssh.insert_key = false
  config.ssh.shell = 'sh -l'

  config.vm.guest = :windows
  config.vm.synced_folder "~/Desktop", "C:/Users/IEUser/Desktop/host-desktop"

  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = "2048"
    vb.customize ['setextradata', :id, 'GUI/ScaleFactor', '2']
  end

  config.vm.define "win7" do |win7|
    win7.vm.box = "IE11-Win7"
  end

  config.vm.define "win8" do |win8|
    win8.vm.box = "IE11-Win8"
  end

  config.vm.define "win10" do |win10|
    win10.vm.box = "MSEdge-Win10"
  end
end
