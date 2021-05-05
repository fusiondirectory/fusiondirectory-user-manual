Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-postfix
   apt-get install fusiondirectory-plugin-postfix-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-postfix
   yum install fusiondirectory-plugin-postfix-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/postfix-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/postfix-fd.schema
