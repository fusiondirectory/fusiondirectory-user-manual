Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-audit
   apt-get install fusiondirectory-plugin-audit-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-audit
   yum install fusiondirectory-plugin-audit-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/audit-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/audit-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/audit-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/audit-fd-conf.schema

