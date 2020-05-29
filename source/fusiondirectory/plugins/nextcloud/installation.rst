Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-nextcloud
   yaourt -S fusiondirectory-plugin-nextcloud-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-nextcloud
   apt-get install fusiondirectory-plugin-nextcloud-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-nextcloud
   yum install fusiondirectory-plugin-nextcloud-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/nextcloud-fd.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/nextcloud-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/nextcloud-fd.schema
