Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-archive
   apt-get install fusiondirectory-plugin-archive-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-archive
   yum install fusiondirectory-plugin-archive-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/ldap/schema/fusiondirectory/archive-fd.schema
   fusiondirectory-schema-manager --install-schema /etc/ldap/schema/fusiondirectory/archive-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/openldap/schema/fusiondirectory/archive-fd.schema
   fusiondirectory-schema-manager --install-schema /etc/openldap/schema/fusiondirectory/archive-fd-conf.schema

