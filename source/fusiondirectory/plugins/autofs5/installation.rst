Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-autofs5
   apt-get install fusiondirectory-plugin-autofs5-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-autofs5
   yum install fusiondirectory-plugin-autofs5-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/ldap/schema/fusiondirectory/autofs5-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/openldap/schema/fusiondirectory/autofs5-fd-conf.schema
