Vagrant.configure(2) do |config|
config.vm.box = "ubuntu16.04.03-mampp"
config.vm.network "private_network", ip: "192.168.33.10"
config.vm.network "public_network", ip: "192.168.1.10"
config.vm.box_url = "https://www.dropbox.com/s/a1z0f9hj5w0mnef/ubuntu16.04.03-mampp.box?dl=1"
config.vm.synced_folder "public_html/", "/home/vagrant/public_html",
	create: "true",
	type: "nfs",
	owner: "www-data",
	group: "www-data",
	mount_options: ["dmode=777", "fmode=666"]
config.vm.provider "virtualbox" do |vb|
	vb.name = "Ubuntu 16.04.03 - Mampp"
	vb.cpus = "1"
	vb.memory = "2048"
	vb.gui = false
end
config.vm.provision "shell", inline: <<-SHELL
apt update
apt upgrade -y
exit
SHELL
end
