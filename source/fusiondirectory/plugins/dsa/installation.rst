Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-dsa
   apt-get install fusiondirectory-plugin-dsa-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-dsa
   yum install fusiondirectory-plugin-dsa-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/dsa-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/dsa-fd-conf.schema
