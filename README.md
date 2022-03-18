# Hitachi PFRest Ansible Playbooks
*These are not official Hitachi Modules, but modules put together by a community. Based on Hitachi Documentation.*
## Overview:
Provision to and from your favourite hitachi array using sample playbooks that make use of the built-in REST framework native to following arrays at the time:
* Hitachi Virtual Storage Platform 5000 Series
* Hitachi Virtual Storage Platform E Series
* Hitachi Virtual Storage Platform G130, G/F350, G/F370, G/F700, G/F900

Adding a bunch of example workflow templates to the template folder.
## Requirements:
Create a storage.json file. Sample storage.json file below:
{
  "storage_ip": "192.168.0.1",
  "storage_username": "ma---------ce",
  "storage_password": "ra------------ce"
}

This file contains your Hitachi array's SVP adres in the case of Enterprise arrays or one of the controllers in the case of modular arrays. The username/password fields are for a user account native to the array. 
## Known Issues:

## Release Notes:
Version: 00.1:

Initial release, publishing items to Ansible galaxy with an example of creating volume using built in PFRest interface. 

## Example Playbooks:
ansible-playbook templates/workflow_create_volume_from_first_pool.yaml -e "my_volume_label=MyNewVolume my_volume_size_in_gb=12"

ansible-playbook templates/workflow_create_volume_from_first_pool_and_assign_to_hostGroups_matching.yaml -e "my_volume_label=MyNewVolume my_volume_size_in_gb=12 my_host_group=ESX_Host_01"