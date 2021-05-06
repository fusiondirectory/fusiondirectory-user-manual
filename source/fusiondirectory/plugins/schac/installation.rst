Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-schac
   apt-get install fusiondirectory-plugin-schac-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-schac
   yum install fusiondirectory-plugin-schac-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/schac-20150413-1.5.0.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/schac-20150413-1.5.0.schema
