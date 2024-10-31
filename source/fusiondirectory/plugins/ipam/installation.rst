Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-ipam
   apt-get install fusiondirectory-plugin-ipam-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-ipam
   yum install fusiondirectory-plugin-ipam-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/ipam-fd.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/ipam-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/ipam-fd.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/ipam-fd-conf.schema
