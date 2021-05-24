Argonaut Components
===================

Global components
-----------------

Argonaut Libraries
^^^^^^^^^^^^^^^^^^

- argonaut-common : main argonaut library (LDAP, package management)
- argonaut-common-fai : `FAI`_ library needed by various `FAI`_ components of Argonaut

Argonaut Server and Client
^^^^^^^^^^^^^^^^^^^^^^^^^^

- argonaut-server : server that receive orders from FusionDirectory (interact  with clients in JSON RPC)
- argonaut-client : client to interact with argonaut-server
- argonaut-fuse : FUSE tftp component that manage pxelinux.cfg directory and create files for PXE boot from LDAP

Argonaut Modules
^^^^^^^^^^^^^^^^

- argonaut-server-module-fai : `FAI`_ module for argonaut-server, it add FAI deployment functions
- argonaut-server-module-opsi : OPSI module for argonaut-server, it add OPSI deployment functions
- argonaut-fuse-module-fai : `FAI`_ module for argonaut-fuse, create files for PXE boot from LDAP for FAI
- argonaut-fuse-module-opsi : `OPSI`_ module for argonaut-fuse, create files for PXE boot from LDAP For OPSI
- argonaut-dovecot : `Dovecot`_ module that create users directories for the mailbox from FusionDirectory

Argonaut Applications
^^^^^^^^^^^^^^^^^^^^^

- argonaut-ldap2zone : tool that create bind files with information from `FusionDirectory`_
- argonaut-quota : tool that grab quota information from `FusionDirectory`_ and create it on the system
- argonaut-samba : program to create samba share from `FusionDirectory`_
- argonaut-fusiondirectory : program that complement a plugin in `FusionDirectory`_, currently has **argonaut-user-reminder** and **argonaut-clean-audit**

Debian components
-----------------

- argonaut-fai-server : package to install on `FAI`_ server (not in NFSROOT)

  - argonaut-fai-monitor : grab installation status from `FAI`_ and send it to argonaut-server (need argonaut-client)
  - fai2ldif : tool that convert `FAI`_ classes in LDIF that we can insert in LDAP

- argonaut-fai-nfsroot : integration package for FAI NFSROOT

  - argonaut-ldap2fai : create `FAI`_ classes in /var/lib/fai/config from LDAP
  - get-config-dir-argonaut : LDAP method for `FAI`_

- argonaut-fai-mirror

  - argonaut-repository : create script to update local mirrors (cron.daily) that are in FusionDirectory
  - argonaut-debconf-crawler : extract debconf from packages in a distant repository

Centos components
-----------------

- argonaut-fai-monitor : grab installation status from `FAI`_ and send it to argonaut-server (need argonaut-client)
- yumgroup2yumi : convert yumgroups into yumi in a ldif file so it can be imported into FusionDirectory `FAI`_ management interface

.. _FAI : https://fai-project.org/
.. _OPSI : https://opsi.org/
.. _Argonaut : https://www.argonaut-project.org/
.. _FusionDirectory : https://www.fusiondirectory.org/
.. _Dovecot : https://dovecot.org/
.. _Bind : https://www.isc.org/downloads/bind/
.. _API : https://fusiondirectory-developer-documentation.readthedocs.io/en/latest/api/index.html
