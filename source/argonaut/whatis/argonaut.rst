What is Argonaut ?
==================

`Argonaut`_ is the companion of `FusionDirectory`_ , is goal is to allow
the management of services and integrate the deployment system(s)
from `FusionDirectory`_.

Features
^^^^^^^^

`Argonaut`_ is composed of a client **Argonaut Client** and a server **Argonaut Server**

Both client and server sides can load modules at start, those modules are strongly related to a FusionDirectory plugin.

Modules can be classified into three categories :

- FusionDirectory integration

 - argonaut-user-reminder to manage the accoun reminder plugin of `FusionDirectory`_
 - argonaut-clean-audit to clean the audit branch of `FusionDirectory`_

- Services management

 - argonaut-ldap2zone: update a dns zone, create view, create acls for `Bind`_
 - argonaut-quota: apply a quota
 - argonaut-dovecot: create the mailbox quota and applies it `Dovecot`_
 - argonaut-fuse :  create on the fly pxelinux.cfg file that matches the type of machine to be deployed, allowing automatic boot during an install by pxe
 
- Integration with deployment tools

 - `FAI`_
 
  - argonaut-fai-nfsroot :  Tools, queues and status management for `FAI`_ (Fully Automated Install) installations.
  - argonaut-fai-mirror: create a synchronization script Mirror of debian or RPM packages
  - argonaut-fai-monitor: follow `FAI`_ installation and report states to `FusionDirectory`_
  - argonaut-fai-server : Argonaut server module to manage `FAI`_

 - `OPSI`_
 
  - argonaut-server-module-opsi : queues, profiles management
 
.. _FAI : https://fai-project.org/
.. _OPSI : https://opsi.org/
.. _Argonaut : https://www.fusiondirectory.org/argonaut/
.. _FusionDirectory : https://www.fusiondirectory.org/
.. _Dovecot : https://dovecot.org/
.. _Bind : https://www.isc.org/downloads/bind/
.. _API : https://fusiondirectory-developer-documentation.readthedocs.io/en/latest/api/index.html

