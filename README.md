create_user
=========

create a user and upload ssh public key for remote authentication

Requirements
------------

No specific required Ansible
Need a default ssh public key or a specific key needs to be called out in a variable.

Role Variables
--------------
#create_user/defaults/main.yml
#Define the you would like to create
user_name: default
#Define de user state absent or present
user_state: present
#Define the path to the ssh public key
ssh_key: ~/.ssh/id_rsa.pub

Dependencies
------------

None

Example Playbook
----------------

- hosts: all
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: robert
         ssh_key: ~/.ssh/cloud_key.pub

License
-------

MIT

Author Information
------------------

leandro.aurelio@brainns.net
