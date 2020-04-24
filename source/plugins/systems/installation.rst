Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-systems
   yaourt -S fusiondirectory-plugin-service-fd.schema
   yaourt -S fusiondirectory-plugin-systems-fd-conf.schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-systems
   apt-get install fusiondirectory-plugin-service-fd.schema
   apt-get install fusiondirectory-plugin-systems-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-systems
   yum install fusiondirectory-plugin-service-fd.schema
   yum install fusiondirectory-plugin-systems-fd-conf.schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/service-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/systems-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/systems-fd-conf.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/service-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/systems-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/service-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/systems-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/systems-fd-conf.schema
