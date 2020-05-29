Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-mail
   yaourt -S fusiondirectory-plugin-mail-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-mail
   apt-get install fusiondirectory-plugin-mail-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-mail
   yum install fusiondirectory-plugin-mail-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/mail-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/mail-fd-conf.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/mail-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/mail-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/mail-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/mail-fd-conf.schema
