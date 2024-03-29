ansible-role-systemd-resolved
=============================

**Note: Due to systemd-resolved 219 in EL 7.2 not resolving short
  names, it is unusable for our present needs, and this project is on
  hold for the time being.**

Configures systemd-resolved, a caching DNS resolver.

The approach generally is designed to be as minimally intrusive as
possible, and except for systemd-resolved itself, the only thing it
needs to change is /etc/nsswitch.conf. The approach is generally the
same as for Ubuntu 16.10+ as explained at
https://lists.ubuntu.com/archives/ubuntu-devel/2016-May/039350.html

That is, /etc/resolv.conf is NOT a symlink to one of the
systemd-resolved files, and thus systemd-resolved will use it to
figure out the upstream DNS servers.

Requirements
------------

This role does NOT configure nsswitch.conf, you must use something
else for that,
e.g. https://github.com/CSCfi/ansible-nsswitch

Role Variables
--------------

Using ansible-role-nsswitch to set up nsswitch.conf systemd-resolved
can be enabled with

<pre><code>
nsswitch_hosts:
	- files
	- resolve
	- dns
	- myhostname
</code></pre>

Dependencies
------------

E.g. ansible-role-nsswitch to set up nsswitch.conf.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: ansible-role-systemd-resolved }

License
-------

MPL 2.0

Author Information
------------------

https://github.com/jabl
