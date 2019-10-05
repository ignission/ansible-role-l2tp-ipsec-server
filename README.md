Ansible Role: l2tp-ipsec-server
=========

[![Build Status](https://travis-ci.org/shomatan/ansible-nginx.svg?branch=master)](https://travis-ci.org/shomatan/ansible-l2tp-ipsec-server)

Installs L2TP/IPsec server.

Requirements
------------

None.

Role Variables
--------------

    l2tp_ipsec_server_host: vpn.example.com
    l2tp_ipsec_PSK: pre_shared_key
    l2tp_ipsec_mtu: 1410
    l2tp_ipsec_mru: 1410
    l2tp_ipsec_server_bind_interface: eth0
    l2tp_ipsec_server_local_ip: 192.168.1.1
    l2tp_ipsec_server_ip_range: 192.168.1.128-192.168.1.254
    l2tp_ipsec_server_dns: 8.8.8.8
    l2tp_ipsec_server_users: []
    l2tp_ipsec_server_firewall_zone: public
    l2tp_ipsec_server_udp_ports: [ 1701,500,4500 ]

Dependencies
------------

- shomatan.epel (RHEL)
- shomatan.firewalld (RHEL)
- shomatan.ufw (Debian)

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

Shoma Nishitateno