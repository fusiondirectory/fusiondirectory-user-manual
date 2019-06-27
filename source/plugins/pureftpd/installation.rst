Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-pureftpd
   yaourt -S fusiondirectory-plugin-pureftpd-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-pureftpd
   apt-get install fusiondirectory-plugin-pureftpd-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-pureftpd
   yum install fusiondirectory-plugin-pureftpd-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/pureftpd.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/pureftpd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/pureftpd.schema
