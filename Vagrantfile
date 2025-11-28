Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/focal64"

    # Adresse IP fixe pour que jenkins puisse trouver la vm
    config.vm.network "private_network", ip:"192.168.56.15"

    # Provisioning : Installation automatique de docker dans la VM
    config.vm.provision "shell", inline: <<-SHELL
        apt-get update
        apt-get install -y docker.io docker-compose
        usermod -aG docker vagrant
    SHELL
end