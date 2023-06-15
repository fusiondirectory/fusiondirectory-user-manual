Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-subcontracting
   apt-get install fusiondirectory-plugin-subcontracting-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-subcontracting
   yum install fusiondirectory-plugin-subcontracting-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/subcontracting-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/subcontracting-fd.schema
