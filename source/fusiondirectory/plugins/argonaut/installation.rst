Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-argonaut
   apt-get install fusiondirectory-plugin-argonaut-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-argonaut
   yum install fusiondirectory-plugin-argonaut-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/service-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/argonaut-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/service-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/argonaut-fd.schema
