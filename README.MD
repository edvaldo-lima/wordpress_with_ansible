
Building a simple stack and deploying Wordpress, MySQL and Apache using vagrant to provision the VMs & Ansible Playbooks.

Requirements:

  1. Vagrant file to create 2 VMs, ubuntu_wordpress and ubuntu_mysql running ubuntu/trusty 64 bits.
  2. Run vagrant up wordpress mysql to provisoon the VMs.
  3. Requires ansible installation.

       - sudo apt update
       - sudo apt install software-properties-common
       - sudo apt-add-repository --yes --update ppa:ansible/ansible
       - sudo apt install ansible

These playbooks require Ansible 2.9.6

These playbooks are meant to be a reference and starter's guide to building Ansible Playbooks.

These playbooks were tested on Ubuntu 18.04 so I recommend that you use Ubuntu to test these modules.

This LAMP stack can be on a single node or multiple nodes. The inventory file 'hosts' defines the nodes in which the stacks should be configured.

    [wordpress]
    wp_server_names

    [database]
    db_servernames

The stack can be deployed using the following command:

    ansible-playbook -i hosts provisioning.yml

Once done, you can check the results by browsing to the ip of the wordpress VM.

You should see a simple Wordpress test page.


