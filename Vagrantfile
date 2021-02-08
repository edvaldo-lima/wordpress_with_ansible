# define imagem(box)
Vagrant.configure ("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 1024
  end

  # cria wordpress VM com ip publico
  config.vm.define "wordpress" do |wordpress|
    wordpress.vm.network "public_network", ip: "10.0.0.74"

    # define provider, config padrão, memoria 1GB e nome da VM wordpress
    wordpress.vm.provider "virtualbox" do |vb|
      vb.name = "ubuntu_wordpress"
    end
  end

  # cria mysql VM com ip publico
  config.vm.define "mysql" do |mysql|
    mysql.vm.network "public_network", ip: "10.0.0.76"

    # define provider, config padrão, memoria 1GB e nome da VM mysql
    mysql.vm.provider "virtualbox" do |vb|
      vb.name = "ubuntu_mysql"
    end
  end
end
