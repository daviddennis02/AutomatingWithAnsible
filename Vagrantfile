Vagrant.configure("2") do |config|
    config.vm.box = "centos/7"

    config.ssh.insert_key = false

    config.vm.provider "virtualbox" do |v|
        v.memory = 2048
        v.cpus = 1
    end

    config.vm.hostname = "test1.example.com"
    config.vm.network "forwarded_port", guest: 80, host: 8000
    config.vm.provision "ansible" do |ansible|
        ansible.playbook = 'playbook.yml'
    end
end