Vagrant.configure(2) do |config|
    # Define base config that all others work from
    config.vm.box = "ubuntu/trusty64"

    # Config
    config.vm.network :forwarded_port, guest: 80, host: 8081
    config.vm.network "private_network", ip: "10.0.6.100"
    config.vm.define :www do |www|
    end

    # Provisioning
    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "vagrant.yml"
        ansible.sudo = true
        ansible.groups = {
            "www" => ["www"],
            "vagrant" => ["www"]
        }
    end
end