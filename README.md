Role Name
=========

[![Build Status](https://travis-ci.org/shomatan/ansible-nginx.svg?branch=master)](https://travis-ci.org/shomatan/ansible-l2tp-ipsec-server)

Installs L2TP/IPsec server.

Requirements
------------

None.

Role Variables
--------------

None.

Dependencies
------------

- shomatan.epel
- shomatan.firewalld

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: shomatan.l2tp-ipsec-server }

License
-------

BSD, MIT

Author Information
------------------
