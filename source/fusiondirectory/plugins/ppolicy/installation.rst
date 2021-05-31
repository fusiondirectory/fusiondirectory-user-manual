Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-ppolicy
   apt-get install fusiondirectory-plugin-ppolicy-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-ppolicy
   yum install fusiondirectory-plugin-ppolicy-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/ppolicy-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/ppolicy-fd-conf.schema
