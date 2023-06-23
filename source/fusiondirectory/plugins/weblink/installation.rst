Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-weblink
   apt-get install fusiondirectory-plugin-weblink-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-weblink
   yum install fusiondirectory-plugin-weblink-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/weblink-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/weblink-fd.schema
