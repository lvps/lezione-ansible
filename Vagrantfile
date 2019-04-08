Vagrant.configure("2") do |vagrant|

  ENV["LC_ALL"] = "en_US.UTF-8"

  vagrant.vm.define "vm1" do |config|
	  config.vm.box = "ubuntu/bionic64"
	  config.vm.hostname = "vm1.example.local"

	  config.vm.synced_folder ".", "/vagrant", disabled: true

	  config.vm.network "private_network", ip: "10.1.1.101"

	  config.vm.provider "virtualbox" do |v|
		  v.name = "lezione-vm1"
	  end

 	  config.vm.provision "ansible" do |ansible|
# 		 ansible.verbose = "v"
 		 ansible.compatibility_mode = "2.0"
		 ansible.playbook = "playbook-0.yml"
		 ansible.extra_vars = { ansible_python_interpreter:"/usr/bin/python3" }
 	  end
  end

  vagrant.vm.define "vm2" do |config|
	  config.vm.box = "ubuntu/bionic64"
	  config.vm.hostname = "vm2.example.local"
	  config.vm.synced_folder ".", "/vagrant", disabled: true
	  config.vm.network "private_network", ip: "10.1.1.102"

	  config.vm.provider "virtualbox" do |v|
		  v.name = "lezione-vm2"
	  end

	  config.vm.provision "ansible" do |ansible|
		  ansible.compatibility_mode = "2.0"
		  ansible.playbook = "playbook-0.yml"
		  ansible.extra_vars = { ansible_python_interpreter:"/usr/bin/python3" }
	  end
  end

  vagrant.vm.define "vm3" do |config|
	  config.vm.box = "ubuntu/bionic64"
	  config.vm.hostname = "vm3.example.local"
	  config.vm.synced_folder ".", "/vagrant", disabled: true

	  config.vm.network "private_network", ip: "10.1.1.103"
	  config.vm.provider "virtualbox" do |v|
		  v.name = "lezione-vm3"
	  end

	  config.vm.provision "ansible" do |ansible|
		  ansible.compatibility_mode = "2.0"
		  ansible.playbook = "playbook-0.yml"
		  ansible.extra_vars = { ansible_python_interpreter:"/usr/bin/python3" }
	  end
  end


end
