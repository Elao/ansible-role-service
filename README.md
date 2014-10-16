Ansible Role - Service
======================

A service role for elao symfony standard vagrant box

Requirements
------------

This role only run on elao symfony standard vagrant box. See https://vagrantcloud.com/elao/symfony-standard-debian


Role Variables
--------------

    elao_services:          # Array of services
      foo:                    # Service name
        project:   foo        # Service project (used to prefix task name, logs and set directory)
        type:      command    # Service type (command|node|symfony)
        command:   bar        # Service command
        directory: /srv/foo   # Service directory
        numprocs:  1          # Service numprocs


Example Playbook
----------------

    - hosts: servers
      vars:
        elao_services:
          foo: { type: node, path: /srv/foo.js }
          bar: { type: command, command: /bin/bar }
          bar: { type: symfony, command: cache:clear, directory: /srv/foo }
      roles:
         - { role: elao.service }


License
-------

MIT


Author Information
------------------

http://www.elao.com/
