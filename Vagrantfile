Vagrant.configure("2") do |config|  
  
  config.vm.provision "shell", path: "setup.sh"

  config.vm.define "node1" do |node1|
    node1.vm.box = "centos/7"
    node1.vm.hostname = 'node1'
    node1.vm.box_url = "centos/7"
 
    node1.vm.network :private_network, ip: "192.168.56.101"
    node1.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--memory", 2560]
      v.customize ["modifyvm", :id, "--name", "node1"]
      v.cpus = 2
    end

  end

end
