Vagrant.configure(2) do |config|
config.vm.box = "ubuntu16.04.03-mampp"		#Nombre de la maquina en la carpeta VirtualBox
config.vm.network "private_network", ip: "192.168.33.10"
config.vm.network "public_network", ip: "192.168.1.10"
config.vm.box = "paulvilla/mampp"		#No editar ya que es el nombre de la Box, y sino no se descargará
config.vm.box_version = "1.0.0"			#Versión que utilizaremos: https://app.vagrantup.com/paulvilla/boxes/mampp
config.vm.synced_folder "public_html/", "/home/vagrant/public_html",
	create: "true",
	type: "nfs",
	owner: "www-data",
	group: "www-data",
	mount_options: ["dmode=777", "fmode=666"]
config.vm.provider "virtualbox" do |vb|
	vb.name = "Ubuntu 16.04.03 - Mampp"	#Nombre de la maquina en el programa VirtualBox
	vb.cpus = "1"				#Numero de CPUs a usar
	vb.memory = "2048"			#Mbs de la RAM a usar
	vb.gui = false				#No se vera la ventada de la maquina al iniciarla (false/true)
end
config.vm.provision "shell", inline: <<-SHELL
apt update
apt upgrade -y
exit
SHELL
end
