Installation
============

In order to install renater-partage plugin, you need to have installed and configured mail plugin.

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-renater-partage
   apt-get install fusiondirectory-plugin-renater-partage-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-renater-partage
   yum install fusiondirectory-plugin-renater-partage-schema

Insert schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/openldap/renater-partage-fd.schema
   
RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/openldap/renater-partage-fd.schema
