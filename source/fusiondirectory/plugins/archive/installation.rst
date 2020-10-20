Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-archive
   yaourt -S fusiondirectory-plugin-archive-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-archive
   apt-get install fusiondirectory-plugin-archive-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-archive
   yum install fusiondirectory-plugin-archive-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/archive-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/archive-fd-conf.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/archive-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/archive-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/archive-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/archive-fd-conf.schema
   
