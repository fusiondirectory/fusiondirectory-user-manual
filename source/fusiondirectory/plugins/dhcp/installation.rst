Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-dhcp
   apt-get install fusiondirectory-plugin-dhcp-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-dhcp
   yum install fusiondirectory-plugin-dhcp-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/service-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dhcp-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dhcp-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/service-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dhcp-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dhcp-fd.schema
