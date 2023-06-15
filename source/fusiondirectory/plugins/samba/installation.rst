Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-samba
   apt-get install fusiondirectory-plugin-samba-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-samba
   yum install fusiondirectory-plugin-samba-schema

Install schemas
---------------

.. note:: 
   
   The samba plugin depends on the systems plugins so the systems plugins schema should be installed correctly
   
Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/samba-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/samba.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/samba-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/samba.schema
