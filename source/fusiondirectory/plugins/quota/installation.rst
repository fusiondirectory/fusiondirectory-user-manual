Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-quota
   apt-get install fusiondirectory-plugin-quota-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-quota
   yum install fusiondirectory-plugin-quota-schema

Install schemas
---------------

.. note:: 
   
   The quota plugin depends on the systems plugins so the systems plugins schema should be installed correctly

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/quota-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/quota.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/quota-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/quota.schema
