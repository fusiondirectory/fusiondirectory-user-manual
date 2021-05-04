Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-debconf
   apt-get install fusiondirectory-plugin-debconf-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-debconf
   yum install fusiondirectory-plugin-debconf-schema

Install schemas
---------------

.. note:: 
   
   The debconf plugin depends on the systems plugins so the systems plugins schema should be installed correctly
   The debconf plugin depends on the argonaut plugins so the argonaut plugins schema should be installed correctly
   
Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/debconf-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/debconf.schema


RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/debconf-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/debconf.schema
