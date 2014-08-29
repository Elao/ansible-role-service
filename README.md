Ansible Role - Service
======================

A service role for elao symfony standard vagrant box

Requirements
------------

This role only run on elao symfony standard vagrant box. See https://vagrantcloud.com/elao/symfony-standard-debian

Role Variables
--------------

* type: Service type (command, node)
* name: Service name
* path: Service path (for node)
* command: Service command

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: elao.service }

License
-------

MIT

Author Information
------------------

http://www.elao.com/
