Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-freeradius

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-freeradius

Install schemas
---------------

You need to download and insert freeradius official schema: https://github.com/FreeRADIUS/freeradius-server/blob/master/doc/schemas/ldap/openldap/freeradius.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /path/to/freeradius.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /path/to/freeradius.schema
