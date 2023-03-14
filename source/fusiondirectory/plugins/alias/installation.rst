Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-alias
   apt-get install fusiondirectory-plugin-alias-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-alias
   yum install fusiondirectory-plugin-alias-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/ldap/schema/fusiondirectory/alias-fd-conf.schema
   fusiondirectory-schema-manager --install-schema /etc/ldap/schema/fusiondirectory/alias-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/openldap/schema/fusiondirectory/alias-fd-conf.schema
   fusiondirectory-schema-manager --install-schema /etc/openldap/schema/fusiondirectory/alias-fd.schema

