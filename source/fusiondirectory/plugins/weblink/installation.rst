Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-weblink
   apt-get install fusiondirectory-plugin-systems-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-weblink
   yum install fusiondirectory-plugin-systems-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/
   fusiondirectory/systems-fd.schema /etc/ldap/schema/
   fusiondirectory/systems-fd-conf.schema 

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/systems-fd.schema 
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/systems-fd-conf.schema
