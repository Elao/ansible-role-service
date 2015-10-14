WARNING: This role is no longer maintained !!!
==============================================

You are strongly encouraged to switch to the new roles stack on https://github.com/ElaoInfra
--------------------------------------------------------------------------------------------

By the way, this role will remain available on https://github.com/ElaoLegacy
----------------------------------------------------------------------------


Ansible Role - Services
=======================

A services role for elao symfony standard vagrant box

Requirements
------------

This role only run on elao symfony standard vagrant box. See https://vagrantcloud.com/elao/symfony-standard-debian


Role Variables
--------------

    elao_services:          # Array of services
      -
        project:   foo        # Service project (used to prefix task name, logs and set directory)
        name:      bar        # Service name
        type:      command    # Service type (command|node|symfony)
        command:   bar.js     # Service command
        directory: /srv/foo   # Service directory
        numprocs:  1          # Service numprocs


Example Playbook
----------------

    - hosts: servers
      vars:
        elao_services:
          -
            { project: foo, name: bar, type: node, command: bar.js }
          -
            { project: bar, name: foo, type: command, command: foo }
          -
            { project: bar, name: cache, type: symfony, command: cache:clear }
      roles:
         - { role: elao.services }


License
-------

MIT


Author Information
------------------

http://www.elao.com/
