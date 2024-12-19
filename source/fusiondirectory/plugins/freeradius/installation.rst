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

You need to download and insert `freeradius official schema <https://github.com/FreeRADIUS/freeradius-server/blob/master/doc/schemas/ldap/openldap/freeradius.schema>`__

Debian
^^^^^^

Save the file in /etc/ldap/schema/.

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/freeradius.schema

RHEL
^^^^

Save the file in /etc/openldap/schema/.

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/freeradius.schema
