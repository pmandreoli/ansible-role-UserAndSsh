ansible-role-UserAndSsh
=========


Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------
``username``: set username
``GUID``: set user GUID, if you do not want to set a specific GUID for the user omit it, the role will assign it randomly > 1000
``ssh_key``: public key for the user
``present``: bool, if you want to set the key

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

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
    - { role:  <role-path> }

```

License
-------
Apache Licence v2

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
