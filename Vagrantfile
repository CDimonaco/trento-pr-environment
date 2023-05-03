Vagrant.require_version ">= 1.8.0"

Vagrant.configure(2) do |config|

  config.vm.box = "opensuse/Leap-15.4.x86_64"
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
    # ansible.verbose = "-vvv"
  end
  config.vm.provider "libvirt" do |v|
    v.memory = 8096
    v.cpus = 8
  end
  config.vm.network "forwarded_port", guest: 4000, host: 4000
end