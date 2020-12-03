Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-dovecot
   apt-get install fusiondirectory-plugin-dovecot-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-dovecot
   yum install fusiondirectory-plugin-dovecot-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dovecot-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/dovecot-fd.schema
