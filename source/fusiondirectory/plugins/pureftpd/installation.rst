Installation
============

Install packages
----------------

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

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/pureftpd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/pureftpd.schema
