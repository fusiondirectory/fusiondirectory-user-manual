Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-debconf
   apt-get install fusiondirectory-plugin-debconf-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-debconf
   yum install fusiondirectory-plugin-debconf-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/service-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/argonaut-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/debconf-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/debconf.schema


RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/service-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/argonaut-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/debconf-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/debconf.schema
