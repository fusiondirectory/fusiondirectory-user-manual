Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-squid
   apt-get install fusiondirectory-plugin-squid-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-squid
   yum install fusiondirectory-plugin-squid-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/proxy-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/proxy-fd.schema
