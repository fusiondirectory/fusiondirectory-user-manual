Installation
============

Install packages
----------------

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

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/nextcloud-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/nextcloud-fd.schema
