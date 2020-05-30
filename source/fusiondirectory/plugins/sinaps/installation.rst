Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-sinaps
   yaourt -S fusiondirectory-plugin-sinaps-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-sinaps
   apt-get install fusiondirectory-plugin-sinaps-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-sinaps
   yum install fusiondirectory-plugin-sinaps-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/sinaps-fd-conf.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/sinaps-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/sinaps-fd-conf.schema
