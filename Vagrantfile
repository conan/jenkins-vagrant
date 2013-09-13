vagrantfile_api_version = "2"
local_synced_folder = "../../dev"
vagrant_synced_folder = "/home/vagrant/dev"


Vagrant.configure(vagrantfile_api_version) do |config|

    config.vm.provision "chef_solo" do |chef|
        chef.node_name = "jenkins"
        chef.cookbooks_path = "cookbooks"   
        chef.add_recipe ""


        chef.vm.box = 'precise32'
        chef.vm.box_url = 'http://files.vagrantup.com/precise32.box'
        chef.vm.synced_folder local_synced_folder, vagrant_synced_folder
        
    end

end

