Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-repository
   apt-get install fusiondirectory-plugin-repository-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-repository
   yum install fusiondirectory-plugin-repository-schema

Install schemas
---------------

.. note:: 
   
   The repository plugin depends on the systems plugins so the systems plugins schema should be installed correctly

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/repository-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/repository-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/repository-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/repository-fd.schema
