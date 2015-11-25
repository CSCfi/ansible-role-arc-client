[![Build Status](https://travis-ci.org/CSC-IT-Center-for-Science/ansible-role-arc-client.svg)](https://travis-ci.org/CSC-IT-Center-for-Science/ansible-role-arc-client)
ansible-role-arc-client
=========

Installs and configures a Nordugrid ARC Client, installs CA- and CRL-packages

Requirements
------------

Repositories that have the Nordugrid ARC client and the related packages.

Role Variables
--------------

   - fgci\_install: True
     If True then install the FGCI repo for EL7

Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansbible-role-arc-client }

License
-------

MIT

Author Information
------------------

