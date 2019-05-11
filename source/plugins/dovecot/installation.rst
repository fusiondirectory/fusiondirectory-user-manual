Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-dovecot
   yaourt -S fusiondirectory-plugin-dovecot-schema

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

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dovecot-fd.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/dovecot-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/dovecot-fd.schema
