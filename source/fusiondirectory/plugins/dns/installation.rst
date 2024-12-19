Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-dns
   apt-get install fusiondirectory-plugin-dns-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-dns
   yum install fusiondirectory-plugin-dns-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/dns-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/dns-fd.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/dnszone.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/dns-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/dns-fd.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/dnszone.schema
