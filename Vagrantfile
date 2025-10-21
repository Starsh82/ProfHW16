Vagrant.configure(2) do |config|

    N = 1
    (1..N).each do |i|
      config.vm.define "HW16host#{i}" do |node|
        node.vm.box = "ubuntu/jammy64"
        node.vm.synced_folder ".", "/vagrant"
        #node.vm.synced_folder ".", "/vagrant", disabled: true
        node.vm.hostname = "HW16host#{i}"
        node.vm.network "private_network", ip:"192.168.56.1#{i}"
        node.vm.provider "virtualbox" do |vb|
          vb.memory = "1024"
          vb.name = "HW16host#{i}"
          vb.cpus = 1
        end
      end
    end
 
end
