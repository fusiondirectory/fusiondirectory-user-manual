Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-supann
   apt-get install fusiondirectory-plugin-supann-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-supann
   yum install fusiondirectory-plugin-supann-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/internet2.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/supann-2019-11-22.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/supann-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/internet2.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/supann-2019-11-22.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/supann-fd-conf.schema
