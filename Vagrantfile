Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.provision "shell", path:"install_syssaid_reqs.sh"
  config.vm.network "private_network", ip: "192.168.33.10"
  ###################################################################################
  #Sync Windows dir containtng license with a dir in guest machine in the line below#
  ###################################################################################
  config.vm.synced_folder '<drive letter>:\\<Absolute path of dir containing the license file>', '/license'
  config.vm.synced_folder './', '/vagrant/'
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
    vb.cpus = "2"
  end
end
