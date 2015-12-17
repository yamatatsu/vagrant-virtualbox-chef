VAGRANTFILE_API_VERSION = "2"
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu14.04"
  config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"

  # config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.synced_folder "./sync_folder", "/home/vagrant/sync_folder", type: "nfs"

  # config.omnibus.chef_version=:latest

  # config.vm.provision "chef_solo" do |chef|
  #   chef.cookbooks_path = "cookbook-for-rails"
  #   chef.add_recipe "default"
  # end
end
