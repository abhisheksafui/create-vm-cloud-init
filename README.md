Role Name
=========

An ansible role to create Ubuntu or Debian VM from cloud images, taking care of user/password and management interface name,mac connecting it to libvirt default network and setting dhcp ip. 

Requirements
------------
The following 

* Create libvirt pool if it does not exist using ansible role: create-pool
* Create backing image from cloud image using role: create-backing-image
* Create Volume from backing image using role: create-volume

Role Variables
--------------
The folowing variables are mandatory:

      - vm_name: vm-ubuntu-1
      - vm_dir: /home/pocuser/abhishek/vm-ubuntu-1
      - vm_ram_size: 8192
      - vm_vcpus: 8
      - mgmt_if_name: mgmt
      - mgmt_if_mac: 02:0d:80:45:00:01
      - username: cloud
      - password: password
      - disk_pool: default
      - disk_name: vm-ubuntu-1.qcow2
      - network_config_version: 2
    
Dependencies
------------

This role has no dependencies on any other role

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

      - name: Install VM from cloud image
        hosts: localhost
    
        roles:
          role: create-vm-cloud-init
          vars: 
            - vm_name: vm-ubuntu-1
            - vm_dir: /home/pocuser/abhishek/vm-ubuntu-1
            - vm_ram_size: 8192
            - vm_vcpus: 8
            - mgmt_if_name: mgmt
            - mgmt_if_mac: 02:0d:80:45:00:01
            - username: cloud
            - password: password
            - disk_pool: default
            - disk_name: vm-ubuntu-1.qcow2
            - network_config_version: 2
    

License
-------

GPL-V2

Author Information
------------------

Contact Abhishek Safui at abhishek6590@gmail.com
