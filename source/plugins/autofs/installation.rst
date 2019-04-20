Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-autofs
   yaourt -S fusiondirectory-plugin-autofs-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-autofs
   apt-get install fusiondirectory-plugin-autofs-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-autofs
   yum install fusiondirectory-plugin-autofs-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/autofs-fd-conf.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/autofs-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/autofs-fd-conf.schema
