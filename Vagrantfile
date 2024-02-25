Vagrant.configure("2") do |config|

  config.vagrant.plugins = {
    "vagrant-libvirt" => {
      "version" => "0.12.2"
    }
  }

  config.vm.provider :libvirt do |libvirt|
    libvirt.driver = "kvm"
    libvirt.nested = true
    libvirt.management_network_domain = "lab.vagrant"
  end

  config.vm.synced_folder '.', '/vagrant', disabled: true # Disable shared folder

  config.vm.define "all-in-one" do |device|
    device.vm.box = "rockylinux/9" # Doesn't use LVM so easier to resize
    device.vm.hostname = "all-in-one"
    device.vm.provider "libvirt" do |libvirt|
      libvirt.memory = 16384
      libvirt.cpus = 12
      libvirt.machine_virtual_size = 100
    end
  end
end
