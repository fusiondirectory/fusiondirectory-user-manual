Installation
============

Install packages
----------------

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

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/autofs-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/autofs-fd-conf.schema
