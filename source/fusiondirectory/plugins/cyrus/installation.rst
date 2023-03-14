Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-cyrus
   apt-get install fusiondirectory-plugin-cyrus-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-cyrus
   yum install fusiondirectory-plugin-cyrus-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/ldap/schema/fusiondirectory/cyrus-fd.schema


RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/openldap/schema/fusiondirectory/cyrus-fd.schema

