Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-ipmi
   yaourt -S fusiondirectory-plugin-ipmi-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-ipmi
   apt-get install fusiondirectory-plugin-ipmi-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-ipmi
   yum install fusiondirectory-plugin-ipmi-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/ipmi-fd.schema
   
Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/ipmi-fd.schema
  
RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/ipmi-fd.schema
