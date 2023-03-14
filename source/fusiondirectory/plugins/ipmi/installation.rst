Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-ipmi
   apt-get install fusiondirectory-plugin-ipmi-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-ipmi
   yum install fusiondirectory-plugin-ipmi-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/ldap/schema/fusiondirectory/ipmi-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/openldap/schema/fusiondirectory/ipmi-fd.schema
