Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-squid
   yaourt -S fusiondirectory-plugin-squid-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-squid
   apt-get install fusiondirectory-plugin-squid-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-squid
   yum install fusiondirectory-plugin-squid-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/proxy-fd.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/proxy-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/proxy-fd.schema
