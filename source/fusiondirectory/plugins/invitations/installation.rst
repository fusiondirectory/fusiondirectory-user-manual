Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-invitations
   yaourt -S fusiondirectory-plugin-invitations-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-invitations
   apt-get install fusiondirectory-plugin-invitations-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-invitations
   yum install fusiondirectory-plugin-invitations-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/invitations-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/invitations-fd-conf.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/invitations-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/invitations-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/invitations-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/invitations-fd-conf.schema
