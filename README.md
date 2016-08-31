ansible-role-systemd-resolved
=============================

Configures systemd-resolved, a caching DNS resolver.

The approach generally is designed to be as minimally intrusive as
possible, and except for systemd-resolved itself, the only thing it
needs to change is /etc/nsswitch.conf. The approach is generally the
same as for Ubuntu 16.10+ as explained at
https://lists.ubuntu.com/archives/ubuntu-devel/2016-May/039350.html

Requirements
------------


Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

GPLv3

Author Information
------------------

https://github.com/jabl
