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
        - role: shomatan.l2tp-ipsec-server
          # common variables
          l2tp_ipsec_server_host: vpn.my-host.com
          l2tp_ipsec_PSK: presharedkey
          # only vpn-server
          l2tp_ipsec_server_bind_interface: eno1
          l2tp_ipsec_server_local_ip: 10.0.0.1
          l2tp_ipsec_server_ip_range: 10.0.0.11-10.0.0.29
          l2tp_ipsec_server_users:
            - { username: user1, password: password1, ipaddress: 10.0.0.10 }

License
-------

MIT

Author Information
------------------
