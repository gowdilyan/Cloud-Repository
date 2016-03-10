sudo apt-get install virtualbox
sudo apt-get install vagrant
sudo apt-get install virtualbox-dkms


vagrant box add precise32 http://files.vagrantup.com/precise32.box
mkdir vagrant_project1
cd vagrant_project
vagrant init


#Edit the Vagrantfile in this directory and replace
config.vm.box = "precise32"

vagrant up

vagrant box add precise32_1 https://atlas.hashicorp.com/hashicorp/boxes/precise32

--Guest additions Installation
sudo apt-get install virtualbox-guest-utils virtualbox-guest-x11 virtualbox-guest-dkms

--JIRA
https://adlm.nielsen.com/jira/browse/CQ-79
kumara89
nochangE@7


--Jenkins:
Install Java & JDK --Optional sudo apt-get install default-jdk
Download Jenkins
https://www.youtube.com/watch?v=8_D49wo6XKI

--Java installation
sudo apt-get install default-jre
sudo apt-get install default-jdk

--Newuser
sudo adduser goudy

--Ansible Installation
	sudo apt-get install software-properties-common
	sudo apt-add-repository ppa:ansible/ansible
	sudo apt-get update
	sudo apt-get install ansible
	
--OpenSSH
sudo apt-get install openssh-server

--Ansible Video
Vagrant.configure(2) do |config|
config.vm.define "webserver" do |webserver|
	webserver.vm.box="ubuntu/trusty32"
	webserver.vm.network "private_network", ip: "192.168.0.2"
	webserver.vm.hostname="webserver"
end
config.vm.define "ansible" do |ansible|
	ansible.vm.box="ubuntu/trusty32"
	ansible.vm.network "private_network", ip: "192.168.0.254"
	ansible.vm.hostname = "ansible"
end
end