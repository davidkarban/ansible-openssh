openssh
=========

Role installs and configures openssh server. Configuration includes security hardening from:
* Mozilla security guidelines <https://wiki.mozilla.org/Security/Guidelines/OpenSSH#Configuration_2>
* Secure secure shell from @stribika at github.com <https://github.com/stribika/stribika.github.io/wiki/Secure-Secure-Shell>

Most important: There is proper set of HMAC, KEX and ciphers to strengthen sshd security.

Role Variables
--------------
```
# defaults to 22
openssh_port:
# should be list of ip addresses, default is all interfaces 
openssh_listen_addresses: false
```

Example Playbook
----------------

    - hosts: servers
      roles:
         - davidkarban.openssh

TODO
----------------
* Add allowed users/groups by AllowUsers or AllowGroups 

License
-------

Apache Licence 2.0
