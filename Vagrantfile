# declaração das variáveis comuns
$memory = "1024"
$cpu = "1"

# configuração do Vagrant 
Vagrant.configure("2") do |config|
    # configuração comum entre as vms 
    config.vm.provision "shell", inline: "echo Hello, VM funcionando, verificando proximos passos"
    config.vm.box = "hashicorp-education/ubuntu-24-04"

    # configurando a vm que será o nó master
    config.vm.define "master", primary: true do |master|
        master.vm.hostname = "master"
        master.vm.network "public_network", ip: "192.168.18.110"

        master.vm.provider "virtualbox" do |vb|
            vb.name = "master"
            vb.memory = $memory
            vb.cpus = $cpu
        end
        master.vm.provision "shell", path: "instalar_docker.sh"
        master.vm.provision "shell", path: "swarm_init.sh"
    end
    
    #configurando a vm que será o node01 worker
    config.vm.define "node01" do |node01|
        node01.vm.hostname = "node01"
        node01.vm.network "public_network", ip: "192.168.18.111"

        node01.vm.provider "virtualbox" do |vb|
            vb.name = "node01"
            vb.memory = $memory
            vb.cpus = $cpu
        end 
        node01.vm.provision "shell", path: "instalar_docker.sh"
        node01.vm.provision "shell", path: "worker_join.sh"
    end

    # configurando a vm que será o node02 worker
    config.vm.define "node02" do |node02|
        node02.vm.hostname = "node02"
        node02.vm.network "public_network", ip: "192.168.18.112"

        node02.vm.provider "virtualbox" do |vb|
            vb.name = "node02"
            vb.memory = $memory
            vb.cpus = $cpu
        end 
        node02.vm.provision "shell", path: "instalar_docker.sh"
        node02.vm.provision "shell", path: "worker_join.sh"
    end

    # configurando a vm que será o node03 worker
    config.vm.define "node03" do |node03|
        node03.vm.hostname = "node03"
        node03.vm.network "public_network", ip: "192.168.18.113"

        node03.vm.provider "virtualbox" do |vb|
            vb.name = "node03"
            vb.memory = $memory
            vb.cpus = $cpu
        end 
        node03.vm.provision "shell", path: "instalar_docker.sh"
        node03.vm.provision "shell", path: "worker_join.sh"
    end
end