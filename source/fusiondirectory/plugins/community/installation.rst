Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-community
   apt-get install fusiondirectory-plugin-community-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-community
   yum install fusiondirectory-plugin-community-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/ldap/schema/fusiondirectory/community-fd.schema
   fusiondirectory-schema-manager --install-schema /etc/ldap/schema/fusiondirectory/community-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/openldap/schema/fusiondirectory/community-fd.schema
   fusiondirectory-schema-manager --install-schema /etc/openldap/schema/fusiondirectory/community-fd-conf.schema
