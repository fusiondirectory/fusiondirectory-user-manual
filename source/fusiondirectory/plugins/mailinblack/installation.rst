Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-mailinblack
   apt-get install fusiondirectory-plugin-mailinblack-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-mailinblack
   yum install fusiondirectory-plugin-mailinblack-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/mailinblack-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/mailinblack-fd.schema

