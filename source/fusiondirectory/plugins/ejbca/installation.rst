Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-ejbca
   apt-get install fusiondirectory-plugin-ejbca-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-ejbca
   yum install fusiondirectory-plugin-ejbca-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/ldap/schema/fusiondirectory/ejbca-fd*

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/openldap/schema/fusiondirectory/ejbca-fd*
