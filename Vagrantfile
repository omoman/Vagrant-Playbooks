Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  # VM configuration
  config.vm.provider "virtualbox" do |vb|
    # Allocate 2GB of RAM for our VM
    vb.memory = 2048
  end

  # Provision with all our playbooks
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "/Users/manny/Vagrant-Playbooks/site.yml"
    ansible.sudo = true
    ansible.groups = {
        "python-dev"    => ["default"],
        "node-dev"      => ["default"],
        "php-dev"       => ["default"],
        "mongodb-group" => ["default"],
        "mysql-group"   => ["default"],
        "apache-group"  => ["default"]
    }
  end
end
