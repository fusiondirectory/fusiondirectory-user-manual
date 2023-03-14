Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-netgroups
   apt-get install fusiondirectory-plugin-netgroups-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-netgroups
   yum install fusiondirectory-plugin-netgroups-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/ldap/schema/fusiondirectory/netgroups-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/openldap/schema/fusiondirectory/netgroups-fd-conf.schema
