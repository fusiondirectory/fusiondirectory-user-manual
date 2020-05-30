Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-alias
   yaourt -S fusiondirectory-plugin-alias-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-alias
   apt-get fusiondirectory-plugin-alias-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-alias
   yum install fusiondirectory-plugin-alias-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/alias-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/alias-fd.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/alias-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/alias-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/alias-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/alias-fd.schema
   
