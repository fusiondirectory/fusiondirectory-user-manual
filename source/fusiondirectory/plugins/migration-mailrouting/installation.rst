Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-migration-mailrouting
   apt-get install fusiondirectory-plugin-migration-mailrouting-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-migration-mailrouting
   yum install fusiondirectory-plugin-migration-mailrouting-schema

Install schemas
---------------

.. note:: 
   
   The migration-mailrouting plugin depends on the mail plugin so the mail plugin schema should be installed correctly

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/mail-routing.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/mail-routing.schema
