Vagrant.configure("2") do |config|
  config.vm.box = "starboard/ubuntu-arm64-20.04.5"
  config.vm.box_version = "20221120.20.40.0"

  config.vm.provider "vmware_desktop" do |v|
    v.gui = true
    v.vmx["ethernet0.virtualdev"] = "vmxnet3"
  end
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
