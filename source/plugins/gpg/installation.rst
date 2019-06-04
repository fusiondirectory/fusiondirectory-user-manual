Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-gpg
   yaourt -S fusiondirectory-plugin-gpg-schema

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

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/gpg-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/pgp*
   
Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/gpg-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/pgp*
  
RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/gpg-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/pgp*
