Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-freeradius
   apt-get install fusiondirectory-plugin-freeradius-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-freeradius
   yum install fusiondirectory-plugin-freeradius-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/freeradius.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/freeradius.schema
