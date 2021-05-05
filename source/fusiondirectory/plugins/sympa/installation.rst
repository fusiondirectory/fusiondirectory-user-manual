Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-sympa
   apt-get install fusiondirectory-plugin-sympa-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-sympa
   yum install fusiondirectory-plugin-sympa-schema

Install schemas
---------------

.. note:: 
   
   The sympa plugin depends on the systems plugins so the systems plugins schema should be installed correctly

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/sympa-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/sympa-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/sympa-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/sympa-fd.schema
