Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-personal
   yaourt -S fusiondirectory-plugin-personal-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-personal
   apt-get install fusiondirectory-plugin-personal-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-personal
   yum install fusiondirectory-plugin-personal-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/personal-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/personal-fd-conf.schema
   
Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/personal-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/personal-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/personal-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/personal-fd-conf.schema
