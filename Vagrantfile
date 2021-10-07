Vagrant.configure(2) do |config|
config.vm.define :web do |web_config|
  web_config.vm.box = "Ubuntu14.04"
  web_config.vm.network "public_network", ip: "192.168.8.89"
  web_config.vm.hostname = "web"
  web_config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
     vb.gui = true
  
     # Customize the amount of memory on the VM:
     vb.memory = "512"
   end
   web_config.vm.provision :ansible do |ansible|
        ansible.playbook = "apache.yml"
   end
end
config.vm.define :mysql1 do |mysql1_config|
  mysql1_config.vm.box = "Ubuntu14.04"
  mysql1_config.vm.network "public_network", ip: "192.168.8.92"
  mysql1_config.vm.hostname = "mysql1"
  mysql1_config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
     vb.gui = true
  
     # Customize the amount of memory on the VM:
     vb.memory = "512"
   end
   mysql1_config.vm.provision :ansible do |ansible|
        ansible.playbook = "mysql.yml"
   end
end
config.vm.define :mysql2 do |mysql2_config|
  mysql2_config.vm.box = "Ubuntu14.04"
  mysql2_config.vm.network "public_network", ip: "192.168.8.93"
  mysql2_config.vm.hostname = "mysql2"
  mysql2_config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
     vb.gui = true
  
     # Customize the amount of memory on the VM:
     vb.memory = "512"
   end
   mysql2_config.vm.provision :ansible do |ansible|
        ansible.playbook = "mysql.yml"
   end
end
config.vm.define :haproxy do |haproxy_config|
  haproxy_config.vm.box = "Ubuntu14.04"
  haproxy_config.vm.network "public_network", ip: "192.168.8.90"
  haproxy_config.vm.hostname = "lb"
  haproxy_config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
     vb.gui = true
  
     # Customize the amount of memory on the VM:
     vb.memory = "512"
   end
   haproxy_config.vm.provision :ansible do |ansible|
        ansible.playbook = "haproxy.yml"
   end
end
end
