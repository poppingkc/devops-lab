Vagrant.configure("2") do |config|
  config.vm.define "web" do |web|
    web.vm.box = "hashicorp/bionic64"
    web.vm.hostname = "web"
    web.vm.network "private_network", ip: "192.168.56.10"
    web.vm.network "forwarded_port", guest: 80, host: 8080
    web.vm.synced_folder "app", "/home/vagrant/app", create: true
    web.vm.provision "ansible" do |ansible|
      ansible.playbook = "web-playbook.yml"
    end
  end
  config.vm.define "db" do |db|
    db.vm.box = "hashicorp/bionic64"
    db.vm.hostname = "db"
    db.vm.network "private_network", ip: "192.168.56.11"
    db.vm.provision "ansible" do |ansible|
      ansible.playbook = "db-playbook.yml"
    end
  end
end
