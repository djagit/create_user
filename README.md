create_user
=========


create a user and upload an ssh public key for remote authentication

Requirements
------------

No specific required Ansible 
Need a default ssh public key for a specific key needs to be called out in a variable.

Role Variables
--------------
#Define the user you would like to create 
user_name: default
#Define the user state absente or present
user_state: present
#Define the path to the ssh public key
ssh_key: ~/.ssh/id_rsa.pub


Dependencies
------------


Example Playbook
----------------
---
- hosts: all
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: robert
         ssh_key: /root/.ssh/id_rsa.pub
License
-------

MIT

Author Information
------------------
fodil.djamel1@gmail.com
