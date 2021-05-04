Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-fusioninventory
   apt-get install fusiondirectory-plugin-fusioninventory-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-fusioninventory
   yum install fusiondirectory-plugin-fusioninventory-schema

Install schemas
---------------

.. note:: 
   
   The fusioninventory plugin depends on the systems plugins so the systems plugins schema should be installed correctly
   
Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/fusioninventory-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/fusioninventory-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/inventory-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/fusioninventory-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/fusioninventory-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/inventory-fd.schema
