Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-ejbca
   yaourt -S fusiondirectory-plugin-ejbca-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-ejbca
   apt-get install fusiondirectory-plugin-ejbca-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-ejbca
   yum install fusiondirectory-plugin-ejbca-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/ejbca-fd*

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/ejbca-fd*

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/ejbca-fd*
