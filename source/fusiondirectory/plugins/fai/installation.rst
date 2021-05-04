Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-fai
   apt-get install fusiondirectory-plugin-fai-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-fai
   yum install fusiondirectory-plugin-fai-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/service-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/argonaut-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/fai-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/fai.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/service-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/argonaut-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/fai-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/fai.schema
