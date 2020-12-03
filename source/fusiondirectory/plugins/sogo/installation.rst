Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-sogo
   apt-get install fusiondirectory-plugin-sogo-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-sogo
   yum install fusiondirectory-plugin-sogo-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/sogo-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/calEntry.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/calRessources.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/sogo-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/calEntry.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/calRessources.schema
