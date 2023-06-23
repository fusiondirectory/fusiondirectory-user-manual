Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-gpg
   apt-get install fusiondirectory-plugin-gpg-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-gpg
   yum install fusiondirectory-plugin-gpg-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/gpg-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/pgp*

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/gpg-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/pgp*
