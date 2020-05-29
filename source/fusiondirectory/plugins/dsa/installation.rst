Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-dsa
   yaourt -S fusiondirectory-plugin-dsa-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-dsa
   apt-get install fusiondirectory-plugin-dsa-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-dsa
   yum install fusiondirectory-plugin-dsa-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dsa-fd-conf.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dsa-fd-conf.schema
   
RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dsa-fd-conf.schema
