Vagrant Box
===========

This role is designed to be a Vagrant provisioner to create a Ubuntu/Xenial64 for development with Docker Containers.

Updates and upgrades the box to the latest packages.

Installs or makes sure it is installed:

* python2 (python-minimal)
* python3
* python3-apt
* python3-pip
* python3-venv
* build-essential
* pwgen
* rsyslog-gnutls
* aptitude

Adds the ubuntu user to the docker group.

Configures rsyslog to ship logs to papertrail using tls.

Adds `export HOST_IP={ the host ip }` to `/home/ubuntu/.profile`

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
