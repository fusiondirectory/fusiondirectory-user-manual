Installation
============

Install packages
----------------

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

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/personal-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/personal-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/personal-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/personal-fd-conf.schema
