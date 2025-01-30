Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-supann-ext
   apt-get install fusiondirectory-plugin-supann-ext-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-supann-ext
   yum install fusiondirectory-plugin-supann-ext-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/supann-ext-fd.schema

RHEL
^^^^

.. code-block:: bash

    fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/supann-ext-fd.schema