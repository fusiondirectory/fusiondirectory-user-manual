Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-sudo
   apt-get install fusiondirectory-plugin-sudo-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-sudo
   yum install fusiondirectory-plugin-sudo-schema

Install schemas
---------------

.. note:: 
   
   The sudo plugin depends on the systems plugins so the systems plugins schema should be installed correctly

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/sudo-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/sudo.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/sudo-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/sudo.schema
