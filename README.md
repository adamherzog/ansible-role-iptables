iptables
========

 * Install and enable iptables
 * Configure, activate, and save iptables rules

Role Variables
--------------

 * iptables_allowed_tcp_ports: [ 22 ]
 * iptables_allowed_udp_ports: []

    Lists of TCP and UDP ports allowed in.

 * iptables_forwarded_tcp_ports: []
 * iptables_forwarded_udp_ports: []

    Lists of source and destination ports to forward.

    # Forward port 80 to port 8080
    iptables_forwarded_tcp_ports:
      - { src: 80, dest: 8080 }

 * iptables_additional_rules: []

    A list of additional rules to add to iptables. These should be
    complete rules ready to add directly into the list of rules.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: iptables }

