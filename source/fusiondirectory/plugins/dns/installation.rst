Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-dns
   apt-get fusiondirectory-plugin-dns-schema

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

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dns-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dns-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dnszone.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dns-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dns-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dnszone.schema
