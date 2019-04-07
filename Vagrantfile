Vagrant.configure("2") do |vagrant|

  ENV["LC_ALL"] = "en_US.UTF-8"

  vagrant.vm.define "vm1" do |config|
	  config.vm.box = "ubuntu/bionic64"
	  config.vm.hostname = "vm1.example.local"

	  config.vm.synced_folder ".", "/vagrant", disabled: true

	  config.vm.network "private_network", ip: "10.33.0.1"

	  config.vm.provider "virtualbox" do |v|
		  v.name = "lezione-vm1"
		  v.customize ["modifyvm", :id, "--memory", "1024"]
		  #v.customize ["modifyvm", :id, "--cpus", "2"]
		  v.customize ["modifyvm", :id, "--ioapic", "on"]
	  end

# 	  config.vm.provision "ansible" do |ansible|
# 		 ansible.verbose = "v"
# 		 ansible.compatibility_mode = "2.0"
# 		 ansible.playbook = "playbook-ro.yml"
# 	  end
  end

  vagrant.vm.define "vm2" do |config|
	  config.vm.box = "ubuntu/bionic64"
	  config.vm.hostname = "vm1.example.local"

	  config.vm.synced_folder ".", "/vagrant", disabled: true

	  config.vm.network "private_network", ip: "10.33.0.2"

  end


end
