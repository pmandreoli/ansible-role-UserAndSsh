ansible-role-UserAndSsh
=======================
Ansible role to create user and inject SSH keys in Centos and Ubuntu VMs, specifically developed for Laniakea system

Requirements
------------

tested with ansible version 2.9.10

Role Variables
--------------

``username``: set username

``GUID``: set user GUID, if you do not want to set a specific GUID for the user omit it, the role will assign it randomly > 1000

``ssh_key``: public key for the user

``present``: bool, if you want to set the key

Dependencies
------------

No dependencies

Example Playbook
----------------

```
---
- name: role for adding users
  hosts: galaxy
  become: yes
  vars:
    ssh_user: 
      - { name: "username", GUID: "<uid>", ssh_key: "ssh-key.pub", present: "yes" }
      - { name: "username", ssh_key: "ssh-key.pub", present: "yes" }
  roles:
    - role: ansible-role-ssh

```

License
-------
Apache Licence v2

Author Information
------------------

Author: Pietro Mandreoli
Email: pietro.mandreoli@unimi.it
