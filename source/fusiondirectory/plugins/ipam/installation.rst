Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-ipam
   yaourt -S fusiondirectory-plugin-ipam-fd.schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-ipam
   apt-get install fusiondirectory-plugin-ipam-fd.schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-ipam
   yum install fusiondirectory-plugin-ipam-fd.schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/ipam-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/ipam-fd-conf.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/ipam-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/ipam-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/ipam-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/ipam-fd-conf.schema
