Vagrant Box
===========

This role is designed to be a Vagrant provisioner to create a Ubuntu/Xenial64 for development with Docker Containers.

Requirements
------------


Role Variables
--------------

Requires a papertrail_server variable. This should be in the form of logsX and is provided by papertrail. The second variable is papertrail_port which is the port papertrail will listen on for your logs. This is also provided by papertrail.

Dependencies
------------


Example Playbook
----------------

    - hosts: vagrant_box
      roles:
         - { role: tjcim.vagrant-box, tags: 'vagrant-box' }

License
-------

BSD

Author Information
------------------

Trevor Christiansen
