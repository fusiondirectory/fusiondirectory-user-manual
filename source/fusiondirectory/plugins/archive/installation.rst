Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-archive
   apt-get install fusiondirectory-plugin-archive-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-archive
   yum install fusiondirectory-plugin-archive-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/archive-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/archive-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/archive-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/archive-fd-conf.schema

